# Generated status-protocol excerpts (bin/fm-brief.sh at 6cb959a)

## ship (--mode no-mistakes)
```
37-   https:// URL exactly as the forge printed it, never a bare number such as "PR 108"; firstmate
38-   copies that URL from your line rather than assembling one.
39:   A mid-task `working:` line (including setup complete) is nonterminal: do not end the turn
40-   after it unless a `paused:` line declares the wait; otherwise continue the same stage until
41-   a defined `done:` gate under Definition of done.
42-   Use `paused: {what you are waiting on, rough duration}` - distinct from `blocked:` - whenever
43-   you deliberately idle, on a known external wait you expect to clear on its own (an upstream
44-   release, a rate-limit reset, a scheduled window) OR on a long job you launched yourself (a build,
45-   an embed, a validation run, a test suite, a long poll): firstmate then leaves your idle pane alone
46-   and rechecks it on a long cadence instead of treating it as a possible wedge. When you know when
47-   the wait clears, say so in the line with `until <YYYY-MM-DDTHH:MMZ>` (UTC) and firstmate rechecks
48-   at that time instead. If you end a turn while a job you started is still running, append the
49-   `paused:` line FIRST and append `working:` when you pick back up. Bound every wait: re-verify
50-   the job is still alive within minutes rather than parking on it indefinitely, so a dead job
51-   surfaces fast. Use `blocked:` when you are stuck and need help.
```

## scout (--scout)
```
34:   Use `paused: {what you are waiting on, rough duration}` - distinct from `blocked:` - whenever
35-   you deliberately idle, on a known external wait you expect to clear on its own (an upstream
36-   release, a rate-limit reset, a scheduled window) OR on a long job you launched yourself (a build,
37-   an embed, a validation run, a test suite, a long poll): firstmate then leaves your idle pane alone
38-   and rechecks it on a long cadence instead of treating it as a possible wedge. When you know when
39-   the wait clears, say so in the line with `until <YYYY-MM-DDTHH:MMZ>` (UTC) and firstmate rechecks
40-   at that time instead. If you end a turn while a job you started is still running, append the
41-   `paused:` line FIRST and append `working:` when you pick back up. Bound every wait: re-verify
42-   the job is still alive within minutes rather than parking on it indefinitely, so a dead job
43-   surfaces fast. Use `blocked:` when you are stuck and need help.
44-5. If you hit the same obstacle twice, append `blocked: {why}` and stop; firstmate will help.
```

## secondmate charter (--secondmate --no-projects)
```
48-Report only true captain-relevant outcomes or a declared wait by appending one line:
49-   `echo "{state}: {one short line}" >> '/tmp/fm-brief-ev.RJzRRR/state/ev-sm.status'`
50-States: working, needs-decision, blocked, paused, done, failed.
51:Use `paused: {what you are waiting on, rough duration}` (distinct from `blocked:`) whenever your domain deliberately idles, on a known external wait you expect to clear on its own or on a long job you launched yourself, naming when it clears with `until <YYYY-MM-DDTHH:MMZ>` (UTC) when you know; use `blocked:` when you are stuck and need firstmate to act.
52-If you end a turn while a job you started is still running, append the `paused:` line first and `working:` when you pick back up, and bound the wait by re-verifying the job is alive within minutes rather than parking on it indefinitely.
53-Use this only for material phase changes, a captain decision, a real blocker, a failure, work ready for review, or work you landed.
54-Work you landed includes a merge you performed yourself under standing merge authority and one the captain merged on the forge: under that authority nothing is ever \"ready for review\", so a landed merge that goes unreported reaches the captain as silence.
```
