# CYBERWISE - Test Cases (Member 4: QA Tester)

Tester: ______________  Date: ______________  Browser: ______________

Mark each row Pass / Fail after testing. Write bugs in the Bug Log below.

| ID | Feature | Steps | Expected Result | Actual | Pass/Fail |
|----|---------|-------|-----------------|--------|-----------|
| T01 | Navigation | Click every top menu button | Only the chosen page shows; active button is highlighted | | |
| T02 | Home feature cards | Click each feature card on Home | Opens the matching page | | |
| T03 | Name - empty | Leave name blank, click Play Quiz | Error: "Please enter your name." | | |
| T04 | Name - 1 character | Type "A", click Play Quiz | Error: at least 2 characters | | |
| T05 | Name - symbols | Type "Cy@ber", click Play Quiz | Error: letters, numbers and spaces only | | |
| T06 | Name - valid | Type "CyberHero", click Play Quiz | Goes to Quiz page, shows "CyberHero" | | |
| T07 | Cyber tip | Click "Another tip" | A tip is displayed | | |
| T08 | Awareness page | Open Awareness | Text, 3 pillars and 5 habits display correctly | | |
| T09 | Password - empty | Open Passwords, leave box empty | Bar empty, "Type something to begin" | | |
| T10 | Password - weak | Type "123456" | "Very Weak", crack time "instantly", checklist mostly unticked | | |
| T11 | Password - common word | Type "Sunshine2024" | Very Weak (contains a common word) | | |
| T12 | Password - repeated | Type "aaaaaaaaaaaaaaa" | Very Weak | | |
| T13 | Password - strong | Type "blue-tiger-lamp-ocean-92" | "Very Strong", all checks ticked | | |
| T14 | Show/Hide password | Click Show, then Hide | Text is revealed, then hidden again | | |
| T15 | Generator | Click Generate | A random password with the chosen length appears | | |
| T16 | Generator length | Move the slider to 24, Generate | Password is 24 characters | | |
| T17 | Generator no options | Untick all four options, Generate | Message: choose at least one character type | | |
| T18 | Copy | Generate, then click Copy | "Copied to clipboard!" message | | |
| T19 | Copy empty | Refresh, click Copy first | Message: Generate a password first | | |
| T20 | Threats search | Type "wifi" | Shows the Public Wi-Fi threat | | |
| T21 | Threats no result | Type "xyz" | 0 threat(s) found and a "No match" message | | |
| T22 | Threats filter | Click Scams, Malware, Account | Only threats in that category are listed | | |
| T23 | Threat details | Click a threat | Opens details: what it is, warning signs, how to stay safe | | |
| T24 | Privacy tick | Tick 4 tips | Progress shows 4 of 10 (40%), bar grows | | |
| T25 | Privacy persist | Refresh (F5), open Privacy | Ticks are still there | | |
| T26 | Privacy reset | Click Reset Checklist | All ticks cleared, 0 of 10 | | |
| T27 | Quiz start | Click Start Quiz | Question 1/10 with 4 options and a 15 s timer | | |
| T28 | Correct answer | Choose the correct option | Green highlight, "+points", explanation, Next button | | |
| T29 | Wrong answer | Choose a wrong option | Red highlight, correct one shown, lose a heart, streak resets | | |
| T30 | Timeout | Do not answer for 15 s | "Time is up!" message, lose a heart | | |
| T31 | Keyboard | Press 1-4 to answer, Enter for next | Works like clicking | | |
| T32 | 50/50 lifeline | Click 50/50 | Two wrong options hidden; button disabled for the rest of the game | | |
| T33 | Streak bonus | Answer 3+ correctly in a row | Points per answer increase | | |
| T34 | Quiz end - finish | Finish all 10 questions | Final score, correct count and rank title shown | | |
| T35 | Quiz end - game over | Lose all 3 hearts | "Game Over" screen with score | | |
| T36 | Play again | Click Play Again | New questions, score 0, 3 hearts | | |
| T37 | Leave quiz | Start quiz, click another menu button | Round is cancelled; returning shows the Start screen | | |
| T38 | Leaderboard save | Finish a game, open Ranks | Score is listed, highest first | | |
| T39 | Leaderboard persist | Refresh (F5), open Ranks | Scores still there (localStorage) | | |
| T40 | Leaderboard limit | Play 11+ games | Only top 10 displayed | | |
| T41 | Reset leaderboard | Click Reset, confirm | Table empty, Home stats back to 0 | | |
| T42 | Home stats | Play a game, go to Home | Games played, best score, correct answers updated | | |
| T43 | Start without name | Clear browser storage, open Quiz, click Start | Redirects to Home asking for name | | |
| T44 | Sound toggle | Click the speaker icon | Icon changes; sounds muted/unmuted | | |
| T45 | Responsive | Shrink the browser to phone width | Layout stacks; menu wraps; no sideways scrolling | | |

## Bug Log

| Bug # | Related Test | Description | Severity | Reported to | Fixed? | Re-test Result |
|-------|--------------|-------------|----------|-------------|--------|----------------|
| 1 | T20 | Searching "wifi" found nothing because the text says "Wi-Fi". | Low | Aluise (JS) | Yes, search now ignores hyphens and spaces | Pass |
| 2 | T12 | "aaaaaaaaaaaaaaa" was rated Weak with "centuries" to crack. | Medium | Aluise (JS) | Yes, repeated characters now count as one | Pass |

(Add your own bugs below. If you found no other bugs, say so in the presentation.)

## Summary (for the Testing slide)

- Total tests: 45
- Passed: ____
- Failed: ____
- Bugs found / fixed: ____ / ____
- Challenges: ______________________________
