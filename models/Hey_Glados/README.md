# Hey_Glados directory contents

This directory contains assets for a custom "Hey GLaDOS" wake word and a matching text-to-speech voice model.

Contents:
- `GLaDOS_instructuctions.txt` — Plain-text system/prompt instructions describing the GLaDOS-style assistant behavior and safety guidelines.
- `hey_gla_dos.tflite` — TensorFlow Lite model for the custom wake word ("Hey GLaDOS").
- `hey_gla_dos.json` — Model metadata/config for Micro Wake Word (probability cutoff, sliding window, version, etc.).
- `share/piper/glados.onnx` — Piper TTS voice model (ONNX) for the GLaDOS voice.
- `share/piper/glados.onnx.json` — Piper voice configuration describing model parameters (language, phonemes, inference settings).

Nested copy (if present):
- `share/piper/` — Same Piper voice model files mirrored for convenience.

Notes:
- Filenames and structure are intended for use with ESPHome Micro Wake Word and the Piper TTS engine; exact integration steps depend on your environment and are not included here.
