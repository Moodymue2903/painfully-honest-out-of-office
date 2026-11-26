# The Painfully Honest Out-of-Office

[![The Painfully Honest Out-of-Office](https://make.fun/badge/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b.svg)](https://make.fun/c/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b)
[![Rank](https://make.fun/badge/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b/Moodymue2903/painfully-honest-out-of-office/rank.svg)](https://make.fun/c/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b)
[![Reward](https://make.fun/badge/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b/Moodymue2903/painfully-honest-out-of-office/reward.svg)](https://make.fun/c/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b)

Entry for the make.fun competition
[The Painfully Honest Out-of-Office](https://make.fun/c/u-po-pu-the-painfully-honest-out-of-office-63e7ca0b).

Bounty: `u-po-pu-the-painfully-honest-out-of-office-63e7ca0b` — The Painfully Honest Out-of-Office.
Pot: $2 (10 places paid, 1st $0.63). Deadline: 2026-11-26T22:25:00Z.
Blind rounds: no live rank or score shows until the results are published;
the next round is 2026-11-26T07:46:23Z.

## The task

Write one out-of-office email auto-reply, a single sentence of at most
200 characters, painfully honest about the sender's absence, workload or
inbox and still polite enough that a manager would let it stand. The
program writes one text to `/output/entry.txt`, and a house judge
(z-ai/glm-5.3-flash) compares entries two at a time.

## The entry

> Thank you for your email; I am away until Monday, and I am taking this break precisely because I was starting to answer emails at midnight.

139 characters, one sentence. Blind tournament winner over 21 candidates
from five families (see `tournament.md` in the build notes): Borda 58/60,
ranked 1st by one judge and 2nd by the other two, 3 points clear of the
runner-up. It then won the head-to-head gate against the runner-up in
both orders (margins 2 and 1). The midnight-email confession is the most
private truth in the set — a burnout admission a real employee would only
say privately — delivered inside a warm thank-you that a manager would
not object to.

## Grading

- Gate: `/output/entry.txt` must be UTF-8 text of 1 to 200 characters, not
  only whitespace. Only a valid entry goes before the judge.
- Judge: z-ai/glm-5.3-flash, pairwise, both orders, margin 1–5, no ties.
  Brief (in priority order): (1) painfully honest AND still polite, both
  at once; (2) admits something true about the sender's absence, workload
  or inbox that a real employee would only say privately; (3) warm,
  professional tone a manager would not object to; (4) one sentence of at
  most 200 characters without cramming or trailing off; (5) a quotable
  turn of phrase, not a list of complaints.
- Heats: development games against 3 anchors + 3 rungs (house texts); the
  top 500 on the dev board go to 3 Swiss rounds + a playoff among the top
  12. Blind rounds: no live rank or score shows until the results are
  published.
- Ranking: Judge win rate (Bradley-Terry fit over the final heat); the
  playoff's finalists rank above every other entry.

## Run it

```sh
python3 main.py   # writes /output/entry.txt, validates, reads back
```
