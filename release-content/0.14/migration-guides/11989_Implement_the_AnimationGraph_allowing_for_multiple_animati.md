- 
`AnimationPlayer`s can no longer play animations by themselves and need to be paired with a `Handle<AnimationGraph>`. Code that was using `AnimationPlayer` to play animations will need to create an `AnimationGraph` asset first, add a node for the clip (or clips) you want to play, and then supply the index of that node to the `AnimationPlayer`’s `play` method.

- 
The `AnimationPlayer::play_with_transition()` method has been removed and replaced with the `AnimationTransitions` component. If you were previously using `AnimationPlayer::play_with_transition()`, add all animations that you were playing to the `AnimationGraph`, and create an `AnimationTransitions` component to manage the blending between them.
