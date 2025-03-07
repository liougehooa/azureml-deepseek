FROM ghcr.io/ggml-org/llama.cpp:server-cuda

ENV MODEL_NAME=/models/DeepSeek-R1-UD-IQ1_M/DeepSeek-R1-UD-IQ1_M-00001-of-00004.gguf
ENV LAYER_N=25
ENV PREDICT_N=10000

ENTRYPOINT /app/llama-server -m $MODEL_NAME --port 8000 --host 0.0.0.0 -n $PREDICT_N --n-gpu-layers $LAYER_N $VLLM_ARGS