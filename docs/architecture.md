# Architecture

Microphone / VAD -> speech recognition -> context and behavioral policy
-> local language model -> response routing -> TTS / playback -> ROS 2
expression intent.

Perception and attention events feed into an independent policy layer.
Safety-related cancellation, idle behavior and command handling should be
tested outside unconstrained natural-language generation.

Key principles: isolated services, observable state, reversible deployment,
bounded queues, latest-turn precedence and clear audio-input permissions.
