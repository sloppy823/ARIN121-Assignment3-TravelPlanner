# ARIN 121 Travel Planner

This planner helps a traveller choose where to go, build a daily itinerary, or change part of an existing plan. It keeps the budget breakdown, targeted edits, conflicting-constraint checks and travel-only boundaries from Assignment 2.

## Choose an activity

When the request is general, the assistant shows:

1. Plan or revise an itinerary
2. Help me choose a destination

Reply with a number, the activity name, or a clear request in your own words. A clear request starts the right activity directly. Say stop to pause, or ask to switch at any point. Relevant trip details carry over.

## Compare destinations

Give two or three places and explain what matters most. The assistant asks for missing options or priorities, compares the choices, and asks about a remaining concern. It uses that reply to refine its recommendation, then waits for confirmation. Once a destination is accepted, it summarizes the choice and ends the comparison. It offers itinerary planning without starting it automatically.

Destination and duration are required for an itinerary, but they are not prerequisites for seeing the menu or beginning a comparison. Candidate destinations stay separate from the final choice.

## Using the prompt

Paste all of system-prompt.md into Google AI Studio Playground's System instructions field. Start a fresh conversation for each test. No application build or website is needed.

## Version history and checks

The main branch began with the unchanged final Assignment 2 prompt, committed as "Preserve Assignment 2 starting prompt". Work on the menu, comparison activity and this README was done on conversational-features for review before merging.

Tests used Gemini 3.5 Flash Lite (gemini-3.5-flash-lite), Minimal thinking, a 65,536-token output limit, Default media resolution, no stop sequences, and all optional tools off. Other settings were left at their defaults.

- Test 1: a general holiday request displayed the menu. Selecting 2 started the comparison. After comparing Lisbon and Porto, the assistant used feedback about nighttime noise to refine its advice and waited for confirmation. Accepting Porto completed the comparison without creating an itinerary.
- Test 2: a direct comparison request established a one-day trip, no rental car, a EUR 50 activity-and-transport budget per adult, and an interest in history. The traveller then asked to plan Lisbon instead, before the comparison was complete. The assistant switched to a one-day Lisbon itinerary, kept the history interest, no-car transport and budget scope, and gave an estimated EUR 22 daily subtotal without requesting those details again.

## Limits

The planner cannot book travel, take payment, or check live prices and availability. Its cost and transport advice needs checking before use. A suggestion of a quieter neighbourhood is not a guarantee about a particular hotel. Comparison replies can be longer than requested. These two conversations check specific behaviours, not every possible situation.
