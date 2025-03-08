# DeepSeek R1 serving with Azure ML

This is an example of how to serve a DeepSeek distilled models with Azure ML.

## Requirements
Before starting, you should meet the following requirements:

- [Access to Azure OpenAI Service](https://go.microsoft.com/fwlink/?linkid=2222006)
- [Azure ML getting started](https://github.com/Azure/azureml-examples/tree/main/tutorials): Connect to [Azure ML] workspace and get your <WORKSPACE_NAME>, <RESOURCE_GROUP> and <SUBSCRIPTION_ID>.
- [Azure AI Studio getting started](https://aka.ms/azureaistudio): Create a project

- ***[Compute instance - for code development]*** A low-end instance without GPU is recommended: **[Standard_E2as_v4] (AMD 2 cores, 16GB RAM, 32GB storage) or **[Standard_DS11_v2]** (Intel 2 cores, 14GB RAM, 28GB storage, No GPUs) 

## How to get started
1. For serve instance, we recommend `Standard_ND40rs_v2` (8 GPUs, v100).
2. Open the terminal of the CI and run:
    ```shell
    git clone https://github.com/liougehooa/azureml-deepseek.git
    ```
3. Modify the **`config.yml`** file with your Azure ML workspace information.
4. You can deploy the model to Azure ML using vLLM or SGLang.
- **UD-IQ1_M Model**: Run the notebook **`deepseek_aml_llama_cpp_q2.ipynb`**
- **UD-IQ2_XXS Model**: Run the notebook **`deepseek_aml_llama_cpp_r1_m.ipynb`**
- **UD-Q2_K_XL Model**: Run the notebook **`deepseek_aml_llama_cpp_r1_xl.ipynb`**

## License Summary

This sample code is provided under the MIT-0 license. See the LICENSE file.

## References

### Model and Core Technologies
- [DeepSeek R1 GitHub Repository](https://github.com/deepseek-ai/DeepSeek-R1) - Official repository for the DeepSeek R1 model
- [llama.cpp](https://github.com/ggml-org/llama.cpp) - Inference framework for quantized models
- [Unsloth DeepSeek-R1-GGUF](https://huggingface.co/unsloth/DeepSeek-R1-GGUF) - Repository of quantized DeepSeek R1 models
- [Another Repo on DeepSeek R1 Distilled Models with Azure ML](https://github.com/daekeun-ml/deepseek-r1-azureml.git) - Repository of another example of how to serve a DeepSeek model with Azure ML.

### Azure Resources
- [Azure Machine Learning Documentation](https://learn.microsoft.com/en-us/azure/machine-learning/) - Official documentation
- [Azure ML Python SDK v2](https://learn.microsoft.com/en-us/python/api/overview/azure/ai-ml-readme) - SDK reference
- [NDv2-series VMs Overview](https://learn.microsoft.com/en-us/azure/virtual-machines/ndv2-series) - GPU VM specifications
- [Azure ML Online Endpoints](https://learn.microsoft.com/en-us/azure/machine-learning/concept-endpoints) - Managed deployment endpoints

### Tools and Clients
- [OpenAI Python Library](https://github.com/openai/openai-python) - Client library for API integration
- [Hugging Face CLI](https://huggingface.co/docs/huggingface_hub/guides/cli) - Command-line interface for model downloading
- [Azure Identity Library](https://learn.microsoft.com/en-us/python/api/azure-identity/azure.identity) - Authentication tools

### Quantization Resources
- [GGUF Format Specification](https://github.com/ggerganov/ggml/blob/master/docs/gguf.md) - Technical details on GGUF format
- [Model Quantization Overview](https://huggingface.co/docs/optimum/en/concept_guides/quantization) - Principles of model quantization

## Authors
**Jihua Liu**  [Medium](https://medium.com/@liougehooa_64019)

**Dr. Zhang** [Medium](https://medium.com/@klarke4001)
