# Video Transcriber — on-device speech model packs

Model files downloaded on demand by the Video Transcriber Android app. Speech recognition runs entirely on the
phone; these files are only the recognition models. Download URLs:
`https://github.com/nguyen-tam/videotranscriber-models/releases/download/packs-v1/<file>`

| File | Bytes | SHA-256 | Used for | Source / licence |
|---|---|---|---|---|
| `ggml-small-q4_0.bin` | 145,458,015 | `f6099c17a4305c6d173ef90ab6f15150dcbb85332b7831313bf36a378d7c5a85` | English, Spanish | OpenAI Whisper small (MIT), converted to ggml and quantised to Q4_0 with whisper.cpp (MIT) |
| `ggml-small-q4_k.bin` | 145,458,015 | `f10105dcc2ad06310283464e13e1df00377603208f64461f3eff5c50b658a804` | German, Portuguese | OpenAI Whisper small (MIT), ggml Q4_K via whisper.cpp (MIT) |
| `ggml-silero-v6.2.0.bin` | 885,098 | `2aa269b785eeb53a82983a20501ddf7c1d9c48e33ab63a41391ac6c9f7fb6987` | voice activity detection (whisper packs) | Silero VAD v6.2.0 (MIT), ggml conversion from whisper.cpp |
| `silero_vad.onnx` | 643,854 | `9e2449e1087496d8d4caba907f23e0bd3f78d91fa552479bb9c23ac09cbb1fd6` | voice activity detection (sherpa-onnx packs) | Silero VAD (MIT), as distributed by k2-fsa/sherpa-onnx |
| `sherpa-onnx-sense-voice-zh-en-ja-ko-yue-int8-2024-07-17.min.tar.xz` | 153,197,724 | `d9a9ff396156dc891fa7ea49040f49a80ed4628032dc389b4ff387d0b5142080` | Chinese, Cantonese | **SenseVoiceSmall** by FunAudioLLM / Alibaba Group (FunASR Model Open Source License 1.1, see `LICENSE-FunASR-MODEL.txt`), int8 ONNX export by k2-fsa/sherpa-onnx; this archive contains only `model.int8.onnx` and `tokens.txt`, re-compressed with xz. |

Attribution: SenseVoice — FunAudioLLM, "SenseVoice", https://github.com/FunAudioLLM/SenseVoice (model name retained).
Whisper — OpenAI, https://github.com/openai/whisper. whisper.cpp — https://github.com/ggml-org/whisper.cpp.
Silero VAD — https://github.com/snakers4/silero-vad. sherpa-onnx — https://github.com/k2-fsa/sherpa-onnx.

The Vietnamese pack is downloaded from the upstream sherpa-onnx release and is not mirrored here.
