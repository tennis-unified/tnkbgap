# Vietnamese Translation Rules

Repo root: `D:/Github Repos/research-intranet`
Source (English): `docs/...`  →  Destination (Vietnamese): `docs-vi/...` (SAME filename)

## Rules
1. Preserve markdown structure exactly: heading levels, `---` rules, blockquotes,
   tables, lists, and inline HTML `<div style=...>` (translate inner text, keep attributes).
2. YAML frontmatter: keep keys `title` / `description`, translate their VALUES into
   Vietnamese. Never leave an English description.
3. Code fences with box-drawing chars (─│┌┐└┘►▼): translate labels inside,
   keep the fence and box shape.
4. Internal links stay unchanged — filenames remain English.
5. Keep these tennis terms in English: forehand, backhand, serve, volley, topspin,
   slice, drop shot, split-step, kick serve, lob, smash, poaching, tiebreak, deuce,
   ad court, passing shot, moonball, tweener, rally, baseline.
6. Keep player names, author names, book titles, journal names, and URLs verbatim.
7. Keep all numbers and units exactly: N, mph, ms, RPM, °, %, m/s², G, cm, inch, feet.
8. Latin/anatomical terms: keep the term, add a short Vietnamese gloss on first use,
   e.g. "biotensegrity (căng-nén sinh học)".
9. Preserve verbatim: `Henry Pham`, `Phạm Đức Hải`, `Tennis Future Lab`,
   `Chan Si Jin`, `Dantian`, `Wu Wei`, `Dĩ Nhu Khắc Cương`, `Petit Bras`.
10. Natural fluent Vietnamese with correct diacritics. No English sentences left behind.

## Preferred renderings
- non-dominant arm → tay không thuận
- knife slice → cú slice sắc lẹm
- Quiet Eye → Quiet Eye (mắt tĩnh)
- kinetic chain → chuỗi động học
- ground reaction force → lực phản lực từ mặt sân
- hip braking → phanh hông
- scapular retraction → co xương bả vai
- unweighting → giảm tải trọng
- follow-through → kết thúc cú đánh
- soft hands → tay mềm
- shoulder-over-shoulder → vai-qua-vai

## Method
Use `read_file` on the source, then `write_file` to the destination.
Translate the FULL file — never truncate or summarize.
Write each file IMMEDIATELY after translating it, before starting the next one.
Report the byte size written for each file.
