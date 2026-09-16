# Do Not Wake It — Public Playtest

Public distribution repository for the focused prototype playtest.

## Purpose

This repository exposes only the browser playtest build. Research notes and development history remain in the private R&D repository.

## Play

Open the GitHub Pages URL.

- PC: WASD / arrow keys to move, E / Space to steal.
- Smartphone / tablet: landscape orientation, left virtual stick to move, right `盗む` button to steal.

The build records the input device so PC and touch-control evidence can be interpreted separately.

## Test protocol

Do not coach a strategy. The start screen explains only the basic objective and controls.

After the 10-room session, the tester answers four three-choice questions. As soon as all four answers are selected, the session result is queued automatically for the playtest collector.

The submission path uses `navigator.sendBeacon` first so the browser can continue sending when the page is hidden or closed. The same payload is also attempted with `fetch(..., keepalive: true)` while the page remains open. A pending copy is kept in local storage until that confirmation request completes, and it is retried on a later visit if necessary. The collector de-duplicates by random test ID.

When the result screen says `送信を受け付けました。もう画面を閉じて大丈夫です。`, the tester does not need to wait for the slower confirmation request.

The automatically collected record includes gameplay metrics, the four post-play answers, a random test ID, device type, session duration, and per-room behavior logs. It does not ask for the tester's name or email address.

If the browser cannot queue or send the result, a `結果をコピー` fallback is shown so the tester can send the result manually.

## Note

This is a temporary research prototype, not a production build.
