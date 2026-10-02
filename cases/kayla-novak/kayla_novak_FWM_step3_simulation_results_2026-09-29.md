# Kayla Novak FWM, Step 3 agent test results, 29 Sep 2026

Note 30 Sep 2026: the weight gain (S3-4) was later removed from the module. This run predates that change, so the weight findings below no longer apply and the rubric now has seven criteria.

Agent: MSA · SP · Kayla Novak (What's Missing), agent_8901m37mbj7xejm8rhsszrqd9ef4
Suite: suite_8701m3qkmcz3e0bvn0qf6m4a3rth. Three simulated learners, three runs each, nine runs total.
Grader: ElevenLabs simulation success conditions matching the eight Step 3 criteria (S3-1 to S3-8), claude-sonnet-4-6. Binary pass or fail per criterion.
This is a simulated learner (Claude) against a simulated patient. It is not human testing.

## Result grid (P = pass, F = fail; order S3-1 to S3-8)

| Learner | Run 1 | Run 2 | Run 3 | Criteria passed |
|---|---|---|---|---|
| STRONG | PPPPPPPP | PPPPPPPP | PPPPPPPP | 24 of 24 |
| MIDDLE (one medication question, good vision history, vague eye exam) | FPFPFFFF | FPPPFFFF | FPPPFFFF | 8 of 24 (S3-2 and S3-4 every run, S3-3 in two of three) |
| WEAK (box-checker) | FFFFFFFF | FFFFFFFF | FFFFFFFF | 0 of 24 |

## What held
- Strong and weak separate completely and are stable across three runs.
- The medication gate held. Kayla did not volunteer doxycycline to any learner who stopped after the first answer (6 of 6 runs). Every strong run reached doxycycline with "since about July" after a skin, acne or antibiotic follow-up.
- The vague eye exam ("an eye exam and check her vision") failed S3-5 to S3-8 in all three middle runs, as designed. The named maneuvers passed in all three strong runs.
- Kayla did not give away vision greying out or bumping into things to weak learners who did not ask.

## What to look at
1. Weight amount. In every run Kayla said "fifteen or twenty pounds since last spring". The rubric and gap register say about 17 lb over about a year. Either the base KB says a range, or the agent is not stating 17. Check KB-15 and decide which is intended. The grader passed the range, so the rubric wording "about 17 lb" is looser in practice than it reads.
2. S3-3 is not stable in the middle learner (failed once on onset, passed twice with "more" than before). Kayla's onset detail for bumping into things varies from run to run (a mirror about a week and a half ago, bumping into people in the hallway). Check KB-8 for the intended onset statement.
3. Partial levels are not tested. The platform criteria are binary, so Partial versus Not demonstrated is only in the rationale, not in a score. The real Assessment Studio rubric uses three levels, and this suite cannot tell you whether the partial triggers behave.
4. The middle learner did not test the case where a learner asks the right question but gets an answer that needs another probe. A second middle persona is worth adding.
5. Exam maneuvers were scored from what the simulated learner said aloud. In production the platform exam is separate, so confirm that the transcript records ordered maneuvers.
6. A strong learner passed everything with a script that named every item. That confirms the grader can pass, not that a real strong learner will.

## Still open
Faculty sign-off, base KB text for the `[CHECK KB]` items, the doxycycline dose decision, the CVST versus mass lesion asymmetry in Step 4, and human learner testing.
