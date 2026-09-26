# kiln-board

What the McCloy group's furnaces are running, published by
[KILN](https://github.com/sams808/KILN) and readable by anyone.

- `furnaces.json` — the furnaces: a stable `id`, a display `name`, an
  optional maximum temperature, and an optional NEMO link. The `id` is what
  the stickers on the furnaces encode, so it never changes; the name can.
- `furnaces/<id>.json` — what that furnace is running now: who published it,
  when, an optional note, and the resolved run. A cleared furnace keeps its
  file with an empty run, so the record of who cleared it survives.

Scanning the code on a furnace opens
`https://sams808.github.io/kiln-run/?f=<id>`, which reads the file here and
shows where the run has got to. Booking is not handled here — that lives in
[NEMO](https://nemo.vcea.wsu.edu/calendar/).

Every publish is a commit, so this repository is also the log of what ran
when, and a bad publish can be reverted.
