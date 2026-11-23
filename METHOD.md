# Real-Life Patch Notes: The Comedy Changelog — Method

## The entry

> v1.8.5: fixed a bug where the brain replayed an embarrassing moment from 2009 at 3 a.m. instead of sleeping.

108 characters, 108 bytes, one line, inside the 1–160 character gate.

## Why this line won

25 candidates were drafted and compared pairwise against the judge's
published criteria, in order:

1. Single-line patch note for a real-life / human-biology bug, reads as
   comedy.
2. Genuinely funny on a first read — the joke rests on a real comedic idea.
3. Reads like an actual release note: version number, terse engineering
   register, fix stated as if it shipped.
4. Names a specific, recognisable bug of the body or daily life — the reader
   winces and laughs at once.
5. Uses its 160 characters well: no padding, every word working.

The winner scores on all five. The bug is the universal 3 a.m. cringe
replay: instead of sleeping, the brain re-runs an embarrassing moment from
2009 — 17 years old, still rendering in full detail. "2009" is the specific
detail that makes it land (a vague "years ago" would be weaker), and
"instead of sleeping" is the twist: the sleep system itself is the thing
being broken by the bug. The register is a plain changelog line — version,
"fixed a bug where", past-tense fix as shipped. Nothing is padded; every word
does work.

## Finalists it beat

- **Bladder queue** — "v2.7.0: fixed the bug where the bladder sent the
  'urgent' signal 5 minutes after the toilet queue formed." A strong, wincing
  scene, but situational: not everyone has stood in that queue, while
  everyone has had the 3 a.m. replay. Lost on criterion 2 (universality of
  the laugh) by a hair.
- **Stomach exam** — "v1.4.7: fixed a bug where the stomach growled loudest
  during the quietest part of the exam." Specific and wincing, but a single
  beat; the winner has two beats (replay + instead of sleeping).
- **Knee rain** — "v2.3.6: fixed a bug where the knee predicted rain with
  100% accuracy and 0% warning." Funny, but "0% warning" is abstract where
  the winner stays concrete.
- **Foot asleep at the interview** — "v1.3.8: fixed a bug where the foot fell
  asleep during a job interview and refused to stand for the handshake." A
  good scene, but the refusal is one beat and the setup is longer than the
  punchline; the winner is tighter per character (criterion 5).

## What was deliberately avoided

- The kit's own example line (left ear rendering audio 40 ms late) was not
  used: it is the house's example text and may be a reference/anchor text.
- No reuse of the user's earlier winning lines (auto-merge PR, roast tests,
  excuse simulations, feature-off ticket, password-manager roast, out-of-office
  auto-reply, pickup-line confidence score, vacuum load-bearing dust).
- No generic "bug" lines with no specific body/daily-life bug (criterion 4).

## The program

`main.ts` (Node 22, stdlib only) writes the winning line to
`/output/entry.txt` and nothing else. It enforces the gate (1–160 code
points, ≤160 UTF-8 bytes, non-whitespace, exactly one line, no leading or
trailing whitespace) and verifies the written file round-trips byte-identical.
The grader cwd is read-only, so nothing is written relative to it — only
`/output/entry.txt`. `main.ts` was revised twice in-session after its first
full write (byte-length check, then whitespace + byte-length round-trip
verification).

Full candidate list and the pairwise tournament are in
`patch-notes-candidates.md` (outside the work dir).
