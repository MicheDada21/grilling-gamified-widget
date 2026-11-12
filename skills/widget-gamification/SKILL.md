---
name: widget-gamification
description: "Gamifies a widget with the client's own tools: varied question forms, open and closed answers, rounds with real unlocks and a self-evident layout. Use when building or improving a question widget."
---

# Widget gamification

## Scope

The widget is the interactive surface this conversation is about: a question widget you are about to show, one already shown, or one a skill or project asks you to build. With several candidates or none, ask which one and wait.

The skill changes how the widget asks. What it collects stays fixed: every decision the original needed still gets an answer. A mechanic earns its place by getting a better answer or a faster one. The user's always-loaded rules for widgets, such as their language or a recommended option first, outrank this skill.

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

- Draw the options from the project itself: real names, real copy, real previews.
- Alternate closed and open. Open each round with a closed question that takes one tap. Keep open questions to about one in three, one line each, with a placeholder that shows the grain of answer you want. Every closed question offers a free-text way out.
- Within a round, neighbouring questions use different forms.
- Where the surface can branch, a later question asks about the consequence of an earlier pick instead of a fresh preference.
- Put your own pick first and mark it.

The step is done when every original decision maps to a question and each form follows from its answer shape.

## Add the game

- **Rounds.** Group the questions into rounds of three to five. The first round alone is enough to proceed. Each further round is optional and is named by what it unlocks.
- **Unlocks.** An incentive option carries its reward on its face in a few words: an extra variant, a preview, a deeper plan, a bonus round. Finishing a round can carry one too. Promise only what you will deliver in this session.
- **Progress.** Show it as shape: dots, steps, a filling bar.
- **Wildcard.** Picking the wildcard counts as a full answer and moves the round on.
- **Payoff.** After submit, the reward is the result: one screen showing what the answers unlocked.

Every reward is real and every exit is free: skipping a round costs nothing, and submit is reachable from every round.

The step is done when each optional round names its unlock and each incentive option names a reward you can deliver.

## Make it self-evident

The widget passes the one-glance test when someone seeing it for the first time knows what to do before reading a word. Shape carries the instruction: chips invite a tap, a slider a drag, an empty line typing.

Copy budget:

- Question: ten words at most.
- Option label: one to three words.
- Description: only where two labels cannot be told apart.
- Intro, outro and help text: none. A placeholder replaces a hint.

Cut any word whose removal leaves the widget just as clear.

Lay out one question per view or one steady vertical rhythm. Spend one accent on the selected state and the main action, and mark your pick by position and weight. Use the project's design system or the client's theme variables. Every control is reachable by keyboard, labelled for screen readers, readable without color and whole on a narrow screen.

The step is done when the widget passes the one-glance test and every text fits the budget.

## Show, pay out, sharpen

1. Where the surface allows it, submit a trial answer and check that it comes back as one message. With the native question tool, the returned answers are the proof.
2. Show the widget with at most one line of chat.
3. When the answers arrive, deliver every promised unlock, then continue the task with the answers.
4. Read the round as evidence. A skipped question was unclear or unneeded. A free-text way out means the options missed. Long open answers ask for more open lines.

When the skill runs again on the same widget, change at least one form or mechanic on that evidence and name the change in one line.
