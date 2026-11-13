# hudson-wakeword

Custom microWakeWord models for the FutureProofHomes Satellite1 (ESPHome `micro_wake_word`).

- `hey_hudson.json` / `hey_hudson.tflite`: "Hey Hudson", the live slot 1 wake word. Trained 2026-11-12/13 on
  Apple Silicon (microWakeWord-Trainer-AppleSilicon v47.8, 50k synthetic positives, Qwen3 + Piper voices).
  Calibrated cutoff 0.95, sliding window 5: recall 99.7% on validation positives, 0.10 false accepts/hour
  on 9.7 h of ambient audio.
- `hey_alfred.json` / `hey_alfred.tflite`: "Hey Alfred", from TaterTotterson/microWakeWords (V3). Cutoff 0.60.
- `hudson.json` / `hudson.tflite`: bare "Hudson", trained 2026-06-20. RETIRED: weak on "Hey Hudson" and prone
  to false triggers on "Hudson River / Yards". Kept for history.

Each manifest's `model` field is an absolute raw URL to its `.tflite`, fetched at ESPHome compile time.
