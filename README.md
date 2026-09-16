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

After the 10-room session, the tester answers four three-choice questions. As soon as all four answers are selected, the session result is automatically sent to the playtest collector and stored in the Google Sheet used by the project.

The automatically collected record includes gameplay metrics, the four post-play answers, a random test ID, device type, session duration, and per-room behavior logs. It does not ask for the tester's name or email address.

If the browser cannot hand the result to the collector, a `結果をコピー` fallback is shown so the tester can send the result manually.

## Note

This is a temporary research prototype, not a production build.
