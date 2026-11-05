# Benchmark

GPU: NVIDIA RTX 5070 Ti (Direct3D 11), Windows 11
Command: `voice.exe -bench` (11 phrases, warm, best of four runs, GPU otherwise idle)

| Measure | Result |
|---|---|
| Speed (median phrase) | 131.5x real time |
| Speed (all 11 phrases) | 134.7x real time |
| First audio (median) | 4.5 ms |
| All 11 phrases | 33.0 s of speech in 0.245 s |
| Cold start (load model + voices + GPU setup) | 274 ms |
| Output | identical audio on every run with the same seed |
