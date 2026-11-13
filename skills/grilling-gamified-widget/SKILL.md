---
name: grilling-gamified-widget
description: "Builds a visually gamified decision widget with the client's rendering tools: grounded questions, responsive graphics, progress and real unlocks. Use when creating or improving a question widget."
---

# Grilling gamified widget

## Scope

The widget is the question surface this conversation is about: one you are about to show, one already shown, or one a skill or project asks you to build. Infer the target from context; ask when ambiguity would change the work.

The result is a visibly gamified interactive widget that helps the user make informed decisions with less effort. Its graphics and game-like interaction are essential. Preserve the decisions the original needed; choose the visual design, forms and mechanics freely to serve them. The user's always-loaded rules for widgets outrank this skill.

## Read the ground

Read the conversation and the relevant files, history and recorded decisions. Scale the investigation to the request. With no target given, inspect enough context to offer grounded directions.

Look up discoverable facts yourself. Ask about the decisions that remain, grounded in real names, constraints, conflicts or examples from the task.

## Map the decisions

Map what remains as a decision tree, including consequential choices the request leaves implicit.

Each decision goes one of three ways.

| The decision | Goes |
| --- | --- |
| Routine means within your authority, with no material effect on the user's outcome, cost or risk | You decide; state assumptions that affect the result |
| Words can settle it: a name, a scope, a priority, a trade-off | A question |
| It needs something to react to: how a thing looks, feels or flows | A question whose options are previews built from the ground. With no surface that can show them, prototype first and ask after |

Order questions by the **frontier**: decisions whose prerequisites are settled. Questions shown together must be independent. Reveal dependent questions after their prerequisites are answered, through branching or a later round. A running lookup holds back only its dependents. Recompute the frontier from the answers; reopen affected decisions if a dependency was missed.

Keep settled decisions, delegated choices, assumptions and unresolved questions distinct. A skipped optional preference can use a disclosed default; a required decision stays open. Continue independent work while its dependents wait. Split an oversized scope into useful branches.

## Pick the surface

Check the available rendering tools and read the instructions of the surface you choose. Prefer a custom rendered widget, including for closed choices. Where available, load the client's visualization skill, such as `visualize`, and follow its rendering and answer-submission contract.

| Available capability | Surface |
| --- | --- |
| Inline visualization or artifact renderer | Custom interactive widget displayed in the conversation |
| No inline renderer | Self-contained HTML page made accessible through a supported preview or file link, with a main action that copies the answers as one message |
| Brief setup, required approvals, or neither route is usable | Native question tool; state the rendering limitation when it is the fallback |

Native questions can prepare the game; the main experience belongs on the rendered surface whenever available.

## Shape the questions

Match each form to its answer: choices, ranking, sliders, open text or previews. Use variety where it helps the user think, with no quota or required alternation.

- One decision per question, with options that show what each choice changes. Draw them from the ground.
- Every closed question offers a free-text way out. Open fields grow with the answer.
- Offer a wildcard for delegating a choice, distinct from "not clear" and "I don't know". Only explicit delegation hands you the decision. Uncertainty may call for research or a prototype; an unclear question needs a better explanation. Let the user flag it with optional feedback and continue the round, while the decision stays open. On fixed surfaces, free text can carry these distinctions.
- When you have a reasoned recommendation, put it first and mark it, while making the alternatives fair and understandable.

## Add the game

Every answer gets an immediate visible reaction: a selection changes, progress advances, a question reveals or an unlock opens. Keep the game compact for a quick choice and richer for deeper decisions. Invent mechanics and visual expression that fit the task. Respect the user's pace and motion preferences; reduced motion keeps the feedback and game structure.

- **Progress.** Keep progress visible as shape, such as steps, dots or a filling bar. A flag or skip can advance navigation while leaving a decision unresolved.
- **Unlocks.** Offer something useful you will deliver in this session, such as a preview, variant or deeper plan. All options of a decision earn the same reward, including delegation. Required information remains available before the choice.
- **Rounds.** Size rounds for the user's effort and the frontier. Optional rounds name what they add. Submit remains reachable, with unfinished decisions carried forward explicitly.
- **Payoff.** After submit, show a result screen with what the answers unlocked, the decisions settled and any assumptions or open questions that affect the next step.

Every reward is real and every exit is free. Reward useful participation rather than extra work created to earn a reward.

## Make it self-evident

Shape should suggest the action at a glance, and copy should make the consequences understandable. Aim for questions around ten words and labels of one to three words; spend more where clarity needs it. Explain unfamiliar terms and consequential trade-offs. Cut text that adds no understanding.

Use the project's design system or the client's theme. Choose the layout and visual expression for the task. Every control is reachable by keyboard, labelled for screen readers, readable without color and usable on a narrow screen.

## Show, pay out, sharpen

1. For custom surfaces, check that sample answers return accurately through a local trial. Preserve selections, free text, delegation and unresolved flags. With the native question tool, the returned answers are the proof.
2. Display the working widget, with at most one line of chat. Done means the graphical surface is usable and answers can return. If neither rendering route works, state that graphical delivery is unavailable; native questions can continue decision collection without fulfilling the graphical deliverable.
3. Deliver every promised unlock and continue the authorized work using the settled decisions. A correction reopens the affected branch.
4. Revisit unclear questions using the user's feedback: a clearer explanation, a grounded example, a preview or a smaller decision. Change the form when that helps.
5. Treat skips, free text and accepted recommendations as clues, not diagnoses. Judge the interaction by decision quality, effort and follow-up corrections. Adapt when the evidence supports a change.

Inspired by [Matt Pocock's grilling](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md) for the decision tree, frontier and distinction between facts and decisions. Consult the source when reviewing those foundations; this skill is self-contained for execution.
