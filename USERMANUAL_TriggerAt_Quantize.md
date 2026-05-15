# BeatPractice Mini Manual
## Trigger At + Quantize (Evolution Lab)

This guide explains the two most confusing controls in Evolution Lab:
- Trigger At
- Quantize

These controls decide when an evolution action is allowed to happen.

Examples of evolution actions:
- Shift Left / Shift Right / Random Shift
- Next Source / Random Source
- Mutate Notes

## 1) Trigger At: "Where in the bar should I check for a change?"

Trigger At picks a musical location in the loop.

Options:
- End of Cycle: check at the final step of the full loop
- Beat 2: check at the start of beat 2
- Beat 4: check at the start of beat 4
- End A (16-step): check at the end of first half
- End B (16-step): check at the end of second half

Think of Trigger At as a checkpoint.

## 2) Quantize: "What timing grid must be respected?"

Quantize defines the timing resolution that is allowed.

Options:
- Step: any step is allowed
- Beat: only beat boundaries are allowed
- Cycle: only loop-end is allowed

Think of Quantize as a timing filter.

## 3) How They Work Together

Current behavior is strict AND logic:
- The current position must equal Trigger At
- AND it must also pass Quantize
- AND Change Every counter must be ready

If one of these three is not true, no evolution is applied.

So the practical rule is:
- Trigger At says where to look
- Quantize says whether that moment is legal
- Change Every says which occurrence actually changes

## 4) What You Should See on the Circle

When evolution is active:
- A trigger marker indicates the chosen trigger step
- Preview rings show what is expected next
- Outer active notes only update when trigger + quantize + counter all align

If the preview seems active but the outer ring does not change yet, the Change Every counter is often the reason.

## 5) Common Setups That Feel Good

Fast and lively:
- Trigger At: Beat 2
- Quantize: Step
- Change Every: 1

Stable groove changes:
- Trigger At: End of Cycle
- Quantize: Cycle
- Change Every: 1 or 2

Predictable beat-locked changes:
- Trigger At: Beat 2 or Beat 4
- Quantize: Beat
- Change Every: 1+

## 6) Why "Nothing Happens" Sometimes

Some combinations rarely (or never) satisfy both conditions.

Examples:
- Trigger At Beat 2 + Quantize Cycle: usually no change
- Trigger At End A (16-step) + Quantize Cycle: usually no change

If in doubt, start with:
- Trigger At End of Cycle
- Quantize Cycle
- Change Every 1

Then loosen Quantize to Beat or Step for more frequent changes.

## 7) Quick New-User Recipe

If you want to understand the controls quickly:
1. Set Mode A to Shift Right
2. Set Change Every to 1
3. Set Trigger At to End of Cycle
4. Set Quantize to Cycle
5. Press Play and watch one full loop
6. Change Quantize to Beat, then Step, and compare frequency

That one test makes the behavior immediately clear.
