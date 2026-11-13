---
name: widget-gamification
description: "Gamifies a widget with the client's own tools: questions grounded in the codebase, varied forms, open and closed answers, live progress and real unlocks. Use when building or improving a question widget."
---

# Widget gamification

## Scope

The widget is the interactive surface this conversation is about: a question widget you are about to show, one already shown, or one a skill or project asks you to build. With several candidates or none, ask which one and wait.

The widget exists to settle decisions: when it closes, you and the user share one understanding of the work, and the user could defend each choice. The skill changes which questions the widget asks and how it asks them. Every decision the original needed still gets settled. A mechanic earns its place by getting a better answer or a faster one. The user's always-loaded rules for widgets, such as their language or a recommended option first, outrank this skill.

## Read the ground

Before writing a question, do the due diligence on what the user wants to act on: read the conversation, the files and history the request touches, and the decisions already recorded there. With no target given, survey the whole codebase, then open the widget by asking what the user wants to improve, with options drawn from what the survey found.

Everything the ground answers leaves the widget. Each remaining question is built on something you found: a real name, a real file, a real conflict between two parts.

The step is done when no question could be answered by reading the codebase or the conversation.

## Map the decisions

Lay out what remains as a decision tree: each decision branches into the decisions that hang off it. Add the decisions the user is making without noticing: what the request implies, and where work of this kind usually breaks.

Each decision goes one of three ways.

| The decision | Goes |
| --- | --- |
| Every option leads to the same work, or it concerns means that change neither cost nor risk | You decide, and state it as an assumption in the payoff |
| Words can settle it: a name, a scope, a priority, a trade-off | A question |
| It needs something to react to: how a thing looks, feels or flows | A question whose options are previews built from the ground. With no surface that can show them, prototype first and ask after |

Order the questions by the frontier: the decisions whose prerequisites are all settled. A round asks frontier questions only, so no answer in a round changes another question in it. A question that hangs off an open answer waits: as a branch prepared for each pick where the surface can branch, otherwise in a next round built from the answers. A lookup still running holds back only the questions that depend on it.

The first round holds the roots, the decisions the most others hang off. When the tree needs more than three rounds, open with one question on which branch to settle now and park the rest.

The step is done when every decision is an assumption you will state or a question placed after everything it depends on.

## Pick the surface

You have free use of every interactive tool the client offers in this session: the native question tool, an inline widget renderer, a page or artifact publisher, a preview pane. List the ones available and read the current instructions of each one you plan to use; the tools themselves are the source of truth for what they can render.

Choose by the richest interaction the questions need.

| The questions need | Surface |
| --- | --- |
| A few closed choices | Native question tool |
| Sliders, ranking, live previews, reveals, rounds | Widget renderer |
| Any of these, with no renderer in the client | Standalone HTML page whose main button copies the answers as one message |

Chain surfaces when it helps, for example a quick native round, then a rendered round built from its answers.

The step is done when one surface or one sequence is chosen and you have read its instructions in full.

## Shape the questions

Give each question the form that matches the shape of its answer.

| Answer shape | Form |
| --- | --- |
| One of a few | Single-pick chips or cards |
| Several at once | Multi-pick |
| A priority | Drag to rank |
| A trade-off or an amount | Slider between two named poles |
| A taste | This-or-that pairs, or previews side by side |
| A name, a nuance, a reason | One open line |
| No strong view | A wildcard that hands the choice to you |

- One decision per question. Its options lead to different work, so each pick changes what you do next.
- Draw the options from the ground: real names, real copy, real previews.
- Alternate closed and open. Open each round with a closed question that takes one tap. Keep open questions to about one in three, each a field that starts as one line and grows with the answer, with a placeholder that shows the grain of answer you want. Every closed question offers a free-text way out.
- Within a round, neighbouring questions use different forms.
- Every question carries a small "not clear" flag, apart from the wildcard: the wildcard means the user has no strong view, the flag means the question did not land. The flag takes an optional few words on what is unclear, moves the round on like any answer, and comes back in the returned message with the question it marks. On a surface with fixed option slots, the free-text way out carries it.
- Put your own pick first and mark it.

The step is done when every original decision maps to a question and each form follows from its answer shape.

## Add the game

Play at full by default: every answer gets a visible reaction at once. The bar moves, the next question reveals, an unlock opens. When the user asks for a quieter widget, keep the mechanics and drop the motion.

- **Progress.** Keep it in view as shape: dots, steps, a filling bar. It moves on every answer and shows the distance to the next unlock.
- **Unlocks.** A reward pays for effort: an open answer, a finished round, a further round. The control that earns it shows it in a few words: an extra variant, a preview, a deeper plan. The options of one decision pay the same, so the answer stays the user's own. Promise only what you will deliver in this session.
- **Rounds.** A round is one frontier, cut to three to five questions with the roots first. The first round alone is enough to proceed: where the user skips a later round, your picks stand as assumptions. Each further round is optional, shorter than the first and named by what it unlocks.
- **Wildcard.** Picking the wildcard counts as a full answer and moves the round on.
- **Payoff.** After submit, the reward is the result: one screen showing what the answers unlocked, the decisions now settled and the assumptions you made in place of questions.

Every reward is real and every exit is free: skipping a round costs nothing, and submit is reachable from every round.

The step is done when each optional round names its unlock, and every reward pays for effort with something you can deliver.

## Make it self-evident

The widget passes the one-glance test when someone seeing it for the first time knows what to do before reading a word. Shape carries the instruction: chips invite a tap, a slider a drag, an empty line typing.

A question is clear when the user can tell what each option changes. Get there by showing, within the copy budget: name the real thing the question is about, and present each option as what it would produce.

Copy budget:

- Question: ten words at most.
- Option label: one to three words.
- Description: only where two labels cannot be told apart.
- Intro, outro and help text: none. A placeholder replaces a hint.

Cut any word whose removal leaves the widget just as clear.

Lay out one question per view or one steady vertical rhythm. Spend one accent on the selected state and the main action, and mark your pick by position and weight. Use the project's design system or the client's theme variables. Every control is reachable by keyboard, labelled for screen readers, readable without color and whole on a narrow screen.

The step is done when the widget passes the one-glance test, every text fits the budget and each option shows what it changes.

## Show, pay out, sharpen

1. Where the surface allows it, submit a trial answer and check that it comes back as one message. With the native question tool, the returned answers are the proof.
2. Show the widget with at most one line of chat.
3. When the answers arrive, deliver every promised unlock and state each assumption in one line, then continue the task with the answers. A correction from the user reopens that branch in a next round.
4. Keep every flagged question open: it stays the user's decision, and the questions that hang off it wait with it. Ask it again in the next widget from a new angle, using what the user wrote on the flag: another form, an example taken from the ground, a preview of each option, or two smaller questions in its place. Both the wording and the form are new.
5. Read the round as evidence. A skipped question was unclear or unneeded. A free-text way out means the options missed. Long open answers ask for more open lines. A round answered only with your picks held assumptions: state them next time and ask what lies past them. A wildcard on a question of look or feel asks for a preview.

When the skill runs again on the same widget, change at least one form or mechanic on that evidence and name the change in one line.

Inspired by Matt Pocock's grilling skill for the decision tree, the frontier and the split between facts and decisions.
