# Selected research findings

The following summaries concern Qwen3-8B with LoRA SFT in a small synthetic refund environment. The reported counts below were reviewed by the project author using both final responses and complete operations.

## 1. First SFT: execution improved, errors remained

On eight paired complete tasks, the initial model passed **1/8** under joint language-and-operation review, while the first SFT checkpoint passed **5/8**.

The improvement did not establish reliable stopping. Some final replies were accurate even though the model had already attempted an invalid write. This motivated a more specific question about applying known completion state to the next action.

The initial model's automatic operation-only count was different from its joint human-reviewed count. This portfolio uses the latter consistently for this comparison.

## 2. A controlled positive case for stopping

An intervention changed a small number of stopping contexts while retaining their supervised targets and matching actual training exposure. After controlling evaluation-input serialization, complete-task joint passes were **6/8 for the control and 8/8 for the variant**.

Four separate local next-decision cases yielded **0/4 and 4/4**. They examined the next action after a supplied history; they were not four more independently completed tasks.

The complete-task evaluation was a controlled retest of previously seen instances. The result supports this particular intervention on the evaluated cases. It does not show that longer histories are necessary, identify a single internal mechanism, or establish broad generalization.

## 3. A competitive comparison changed the working baseline

The diagnostic scheme D was compared with a conventional demonstration scheme S on eight new paired complete tasks. The schemes shared the base model, initialization and main training budget, while token counts and prior design costs were not identical.

| Measure | D | S |
| --- | ---: | ---: |
| Joint language + operation pass | 6/8 | 8/8 |
| Correct stopping in stopping cases | 2/2 | 2/2 |

D's two failures concerned an omitted evidence-reading obligation in the predeclared task contract. The actual refunds had the correct target, amount and eligibility; no financial loss was observed. The difference therefore supports S's better adherence to this batch's contract, not a general financial-safety advantage.

D had already benefited from earlier diagnosis and successful-design selection. The comparison tested two fixed schemes, rather than isolating the net value of execution information. It also changed several design choices, so the result cannot identify any one choice as the cause.

**Decision: select S as the working baseline and retain the negative result.** A targeted intervention improving an old control did not establish that its design process was more worthwhile than a strong conventional alternative.

## What remains open

All three studies are small and belong to one synthetic environment family. Their task sets and purposes differ; the counts should not be pooled or presented as a single progress curve. No additional RL benefit or general diagnostic superiority has been established.

The next research question concerns when execution evidence changes intervention choices enough to justify its acquisition and interpretation cost. Competitive training and engineering alternatives remain necessary comparators.

This is a high-level summary of retained experiment records. It does not provide source code, raw trajectories or a complete reproduction package.

[Return to the portfolio](../README.md)
