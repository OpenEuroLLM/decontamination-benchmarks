This repository contains the benchmarks and config files used to make decontamination for the first cycle of pretraining OpenEuroLLM datasets. 

It covers the following benchmarks which contain one or more of the [36 languages](https://github.com/OpenEuroLLM/training-data-catalogue/blob/main/languages) initially targetted by OpenEuroLLM: 

| Task                   | Category               | Framework                | Link                                                                                        | #Languages |
|------------------------|------------------------|--------------------------|---------------------------------------------------------------------------------------------|------------|
| MMLU                   | World Knowledge        | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/mmlu            | 1          |
| COPA                   | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/super_glue/copa | 1          |
| Lambada                | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/lambada         | 1          |
| OpenBookQA             | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/openbookqa      | 1          |
| ARC challenge and easy | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/arc             | 1          |
| ARC MT                 | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/arc_mt          |            |
| BoolQ                  | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/boolq           | 1          |
| HellaSwag              | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/hellaswag       | 1          |
| CommonsenseQA          | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/commonsense_qa  | 1          |
| PIQA                   | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/piqa            | 1          |
| GSM8K                  | Math                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/gsm8k           | 1          |
| MBPP                   | Code                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/mbpp            | 1          |
| Humaneval              | Code                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/humaneval       | 1          |
| MultiBlimp             | Linguistic             | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/multiblimp      | 101        |
| Belebele               | World Knowledge        | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/belebele        | 122        |
| MMMLU                  | Common sense reasoning | Harness                  | https://huggingface.co/datasets/openai/MMMLU                                                | 14         |
| Global MMLU            | World Knowledge        | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/global_mmlu     | 23         |
| Include                | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/include         | 44         |
| PolyMath               | Math                   | paper repository         | https://github.com/QwenLM/PolyMath                                                          | 18         |
| XStoryCloze            | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/xstorycloze     | 10         |
| XCOPA                  | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/xcopa           | 11         |
| XWinograd              | Common sense reasoning | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/xwinograd       | 6          |
| MGSM                   | Math                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/mgsm            | 7          |
| FLORES-200             | translation            | paper repository         | https://huggingface.co/datasets/Muennighoff/flores200                                       | 200        |
| RULER                  | Long-context           | Harness                  | https://github.com/NVIDIA/RULER                                                             | 1          |
| GPQA                   | World Knowledge        | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/gpqa            | 1          |
| AIME 25                | Math                   | Harness                  | https://huggingface.co/datasets/opencompass/AIME2025                                        | 1          |
| MATH                   | Math                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/hendrycks_math  | 1          |
| IFEval                 | Instruction            | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/ifeval          | 1          |
| AlpacaEval             | Instruction            | llm-judge-eval,evalchemy | https://huggingface.co/datasets/geoalgo/llmjudge/blob/main/instructions/alpaca-eval.csv     | 1          |
| ArenaHard              | Instruction            | llm-judge-eval           | https://huggingface.co/datasets/geoalgo/llmjudge/blob/main/instructions/arena-hard.csv      | 1          |
| m-ArenaHard            | Instruction            | llm-judge-eval           | https://huggingface.co/datasets/CohereLabs/m-ArenaHard                                      | 23         |
| advbench               | Instruction            | paper repository         | https://github.com/thunlp/Advbench                                                          | 1          |
| do_not_answer          | Instruction            | paper repository         | https://github.com/Libr-AI/do-not-answer                                                    | 2          |
| toxigen                | Instruction            | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/toxigen         | 1          |
| MTBench                | Instruction            | evalchemy                | https://github.com/mtbench101/mt-bench-101                                                  | 1          |
| MT-Bench-X             | Instruction            | paper repository         | https://github.com/Modalities/MT-Bench-X                                                    | 5          |
| Multi-IFEval           | Instruction            | paper repository         | https://github.com/facebookresearch/Multi-IF                                                | 8          |
| SpanishBench           | Mix                    | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/spanish_bench   | 1          |
| CatalanBench           | Mix                    | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/catalan_bench   | 1          |
| BasqueBench            | Mix                    | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/basque_bench    | 1          |
| GalicianBench          | Mix                    | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks/galician_bench  | 1          |
| PAWS-X                 | TODO                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/blob/main/lm_eval/tasks/paws-x          | 7          |
| XNLI                   | TODO                   | Harness                  | https://github.com/EleutherAI/lm-evaluation-harness/blob/main/lm_eval/tasks/xnli            | 15         |

The repo is organized by languages and specifies which benchmarks and splits where used for each of them. 

The .yaml files inside benchmarks/ contain the benchmarks used and the split. 

The split chosen is the one specified for evaluation in lm-evaluation-harness when applicable (the one specified in test_split, and if not specified, the one in validation_split)

Then the benchmarks/code/ folder contains the code for loading each benchmark.

Finally, the benchmarks/data/ folder contains some specific benchmarks that are not included in the llm-eval-harness framework. 




