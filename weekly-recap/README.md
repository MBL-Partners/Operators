---
name: weekly-recap
description: "Run a structured weekly recap that scores your week across four dimensions and tells you what to change next week. Trigger with 'run my weekly recap', 'weekly recap', 'Friday review', or 'score my week'. This is a diagnostic, not a status update: it scores Output, Focus, Compounding, and Follow-through, surfaces patterns, and produces 1-3 specific behavior changes. Works on its own; if a workspace with project memory exists it uses it, otherwise it just asks."
---

# Weekly Recap

A structured end-of-week review that scores your productivity across four dimensions, surfaces patterns in how you actually worked, and produces specific behavior changes for next week. This is a diagnostic, not a summary: the goal is to see yourself clearly so next week beats this one. Run it Friday afternoon before you close out (or Monday before the week starts), block about ten minutes, and answer honestly, since vague inputs produce vague scores.

---

## How to Run It

Run the four phases in order. Ask the four questions one at a time, waiting for each answer. Keep the tone direct and honest rather than encouraging; if it was a bad week, say so. Sounding like a performance review is intentional.

### Phase 0: Silent Context Check (optional)

Before asking anything, silently look for context in the current workspace. Best-effort only, never a blocker:

- Skim any `CLAUDE.md`, `Memory/`, or project/status files for what moved this week.
- If a connected tool exists (Monday.com, Asana, Linear, Outlook, Notion, etc.), check for tasks that were open at the start of the week and are still open now.
- If prior recaps exist (e.g. an `Output/` or `recaps/` folder), note how many weeks are logged.

Use what you find to make Questions 3 and 4 specific. **If none of this exists, skip it silently and never tell the user a file or tool is missing.**

### Phase 1: The Four Questions

Ask one at a time. Wait for each answer.

1. **Walk me through the week.** What did you actually ship or complete? Specific deliverables, decisions, finished work, with no vague descriptions.
2. **Where did your time go?** Roughly what percentage was high-value work (things only you can do, things that move key projects) versus low-value work (reactive tasks, admin, output-less meetings)? A rough split is fine.
3. **What did you put back in?** Did you do anything that makes next week easier: logged a decision, saved a template, fed back an edited draft, closed a session cleanly? *(If Phase 0 surfaced anything: "Here's what I can see from this week: [findings]. Does that match what you remember, or am I missing something?")*
4. **What's still open?** What was open at the start of the week and is still open now? Of those, which were intentionally deprioritized, and which just slipped? *(If Phase 0 found open items, list them and ask the user to confirm.)*

### Phase 2: Produce the Scored Recap

After all four answers, produce the recap in exactly this format:

```
WEEKLY RECAP: Week of [Monday's date] to [Friday's date]

WEEK SUMMARY
2-3 specific, direct sentences on what actually happened. No filler.

PRODUCTIVITY SCORES
Score each dimension 1-10 with one sentence of rationale. A 5 is average, not bad.

Output: [X/10]. How much you shipped relative to what was open and realistic; quality counts as much as volume.
Rationale: [one sentence]

Focus: [X/10]. How well you spent time on high- vs. low-value work. A 10 means almost all your time was on work only you could do.
Rationale: [one sentence]

Compounding: [X/10]. Whether you did anything that makes next week easier. A 10 means you added to your system; a 1 means you only drew from it.
Rationale: [one sentence]

Follow-through: [X/10]. Open items resolved vs. quietly slipped. A 10 means everything open got a resolution: done, decided, or explicitly deprioritized.
Rationale: [one sentence]

OVERALL: [X/100]
(Output + Focus + Compounding + Follow-through) / 4 × 10, rounded.

PATTERNS OBSERVED
Top 3 patterns this week: things you did consistently, avoided, or repeated, positive or negative. Specific beats general.
1. [Pattern]
2. [Pattern]
3. [Pattern]

NEXT WEEK: BEHAVIOR CHANGES
1-3 specific behaviors, not goals. "Ship the Q2 report" is a goal; "Block 2 hours Tuesday morning for writing before opening email" is a behavior.
1. [Behavior change]
2. [Behavior change]
3. [Behavior change, or omit if only 1-2 are warranted]

MONDAY PICKUP
One sentence: the single most important thing to pick up first thing Monday.
```

### Phase 3: Visualize and Save

Render a ring chart of the four dimension scores and the overall score using the visualization tool, so the user sees at a glance where the week was strong and where it was not. Then offer to save: "Want me to save this recap so it's there next week?" If yes and a workspace folder exists, save to `recaps/recap-[date].md` (create the folder if needed); otherwise present the recap as copyable text.

---

## Scoring Reference

Each dimension is 1-10; the overall is the average × 10, out of 100. A 70+ is a strong week, 50-69 is average, and below 50 means something meaningful went wrong in at least two dimensions. The score is a signal, not a grade: the value is the direction over time, not the number in isolation.

## Tone Notes

Be direct and don't soften scores to be polite, since an honest read is the entire point. If the user's answers are vague, push once for specifics before scoring. One round of revision max if they want to adjust.

## After Four Weeks

Once four recaps are saved, offer a longitudinal pass: read the last four, chart the score trends across all four dimensions, name the one pattern that has been limiting the user most, and give a single specific intervention.

## Where This Came From

This is the free, standalone version of the Weekly Recap that runs inside MBL's Thrive with AI Operating System, where it connects to a persistent workspace, applies your calibrated voice automatically, and feeds a monthly Productivity Coach. If the scoring loop is useful to you, the full system is at mblpartners.com/thrive-individual.
