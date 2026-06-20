# hudson-wakeword

Custom microWakeWord models for the FutureProofHomes Satellite1 (ESPHome `micro_wake_word`).

- `hudson.json` / `hudson.tflite` — "Hudson" wake word, trained 2026-06-20 on Apple Silicon
  (microWakeWord-Trainer-AppleSilicon). Synthetic v1. recall 99.9%, ambient_faph ~0.93.
  Calibrated cutoff 0.40, sliding window 3.
- `hey_alfred.json` / `hey_alfred.tflite` — "Hey Alfred", from TaterTotterson/microWakeWords (V3). cutoff 0.60.

Each manifest's `model` field is an absolute raw URL to its `.tflite`, fetched at ESPHome compile time.
