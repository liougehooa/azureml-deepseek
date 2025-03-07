FROM vllm/vllm-openai:latest

ENV MODEL_NAME=deepseek-ai/DeepSeek-R1-Distill-Llama-70B

ENTRYPOINT python3 -m vllm.entrypoints.openai.api_server --model $MODEL_NAME $VLLM_ARGS