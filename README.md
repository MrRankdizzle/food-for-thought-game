# Food for Thought — Little Chute

An original match-three nutrition learning game for high-school students, with Little Chute logos and Carolina blue, sky blue, white and navy styling.

## Try it

Open `index.html` in a browser. The game, questions and images work offline; source links require an internet connection. Click **Answer challenge** to earn moves, then select two neighboring treats to swap. Match three or more horizontally or vertically.

## Game and learning rules

- First-attempt answer: 3 moves if correct, 1 if incorrect. Read the explanation, then choose **Use earned moves**.
- Comeback round: 2 moves once per newly mastered question. Repeated misses do not earn moves.
- Matches score 10 candy points per cleared treat, multiplied by cascade number. Every 1,000 points raises the level.
- Swaps that make no match cost nothing. Boards with no available moves refresh for free. A hint identifies a possible swap.
- Learning XP: 20 for a first attempt, 80 more if correct, plus 25 for each three-answer streak. A newly mastered comeback gives 40 XP. A perfect first run is 2,150 XP and 60 moves.
- The first-run score is preserved during comeback rounds. Badges recognize five attempts, a three-correct streak, completion, and mastery of all 20.
- No timer, student account or public leaderboard. Scores remain in page memory and reset on refresh. This is practice, not a secure exam; the answer key is in the source.

## Activities

Nine questions use activities: fat/product sorting (2, 9); five-food cholesterol ranking (4); budget-step ordering (7); full product Nutrition Facts label with a sodium slider (12); draggable clock hand plus slider (13); a ground-beef package image and portion-fat calculation (15); sodium-limit slider (18); circle-two-foods selection (19). The other eleven use multiple-choice cards with researched explanations.

The clock uses about 20 minutes as the ADA teaching estimate and explains that it is not an exact cutoff. The beef image is generated classroom imagery with a readable 80% lean / 20% fat label. Chromium and protein questions use evidence reasoning and plausible competing nutrition concepts.

Every question has a plain-language explanation and source links. Scientific studies support health claims; manufacturer, FDA, NIH and USDA references support product ingredients, labels and educational guidance. See `TEACHER-NOTES.md` for sources, revisions and image-generation details.

## Controls

Board: mouse/touch selects adjacent tiles; Tab or arrow keys navigate tiles; Enter or Space selects. Sorting supports dragging or tap-to-select/place. Ordering has keyboard-accessible move buttons. Numeric activities have range controls, adjustment buttons and typed input. The clock also supports direct pointer dragging and arrow keys. Reduced-motion preferences are respected. Full browser accessibility testing remains pending.

## Publish through GitHub and Vercel

Upload this folder's contents to the repository root, including `assets`. Import the repository in Vercel; select **Other**, leave the build command unset, and use `.` as the output directory if asked. Deploy and share the URL. [Vercel reference](https://vercel.com/docs/builds/configure-a-build).

## Edit

- `questions.js`: content, explanations, source links, multiple-choice keys.
- `activities.js`: alternative activities and their answer keys (these override MC keys).
- `game.js`: match-three engine and move rewards.
- `app.js`: quiz state, XP, review and game integration.
- `style.css`: layout and branding.
- `assets`: supplied school logos and generated ground-beef image.

The experience is configured for these 20 questions.

## Verification

Syntax and state/markup checks pass for all 20 right/wrong answers, activity grading, clock/number synchronization, XP, badges, first-run versus comeback scoring, move rewards, no duplicate rewards, and resets. Game checks cover 500 generated playable boards, adjacency without row wrapping, horizontal/vertical matches, cascades/refills, locked boards, and free rejection of nonmatching swaps. The beef image text was visually inspected.

The local browser cannot launch in this environment. Actual browser layout, pointer interactions and accessibility are not fully verified; review them in a browser before class. Nothing has been deployed.
