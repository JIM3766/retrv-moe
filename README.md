# Retrv-MoE Evaluation Artifact

This minimal artifact contains the evaluation entry point for the KDD 2026 paper "Retrv-MoE: Scaling Unified Multimodal Retrieval with Sparse Mixture-of-Experts".

## Files

```text
eval/eval_mbeir_moe_lora_binary_alltasks.py
scripts/eval/eval_mbeir_moe_lora_binary_alltasks.sh
checkpoints/README.md
```

## Important

The two evaluation files are not fully standalone. The Python script imports project modules such as:

```text
models.configuration_lora_moe
models.modelling_lora_moe
collators.mbeir_eval
dataset.datasets_mbeir_binary_v2
```

Please include those dependency files/directories from the original project as well.

## Run

```bash
bash scripts/eval/eval_mbeir_moe_lora_binary_alltasks.sh
```

You can override paths without editing the script:

```bash
MODEL_ID=/path/to/retrv_moe_lora \
ORIGINAL_MODEL_ID=/path/to/base_model \
IMAGE_PATH_PREFIX=/path/to/data_binary \
GLOBAL_POOL=/path/to/mbeir_union_test_cand_pool_bin.jsonl \
INSTRUCTIONS=/path/to/query_instructions.tsv \
TASK_CONFIG=./eval/eval_tasks.json \
bash scripts/eval/eval_mbeir_moe_lora_binary_alltasks.sh
```
