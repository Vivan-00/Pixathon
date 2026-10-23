AI tools used--
Claude-- For the research of our problem statement.
elevenlabs-- for sound effects and sound tracks.
Antigravity-- for making the actual game from the propmpt
suno-- For the background music of the puzzle 
Gemini -- For other research purposes

AI tools used--
Claude-- For the research of our problem statement.
elevenlabs-- for sound effects and sound tracks.
Antigravity-- for making the actual game from the propmpt
Pixellab-- Used for the final touchups of the puzzle

Prompts used--
PROMPT1. 
Project Title: THE CIPHER VAULT — Crack the Password

Act as an expert puzzle designer and game mechanic designer,. Build a complete, playable, browser-based puzzle game in which the player must solve a sequence of interconnected puzzles to discover a secret password and unlock a vault.

This is a project based on the theme **“Puzzle Passwords.”** The password must be the puzzle itself, not merely a login form.

Do not just create a visual prototype. Implement the actual puzzle logic, answer validation, progressive difficulty, live feedback, level progression, and a proper victory screen.

 1. Core Game Concept

The player discovers a mysterious digital vault protected by an encrypted password. The password has been divided into hidden pieces, and each piece can be discovered by solving a different puzzle.

The vault contains eight puzzle chambers. Each chamber tests a different skill, such as logical reasoning, riddles, pattern recognition, decoding, mathematics, or deduction.

Every solved chamber reveals a password fragment or an important rule. Once all eight chambers are completed, the player must assemble the final password while satisfying all the password rules.

**The twist:** Players are not simply guessing a password. They are discovering how the password was constructed.

The game should feel like an escape room combined with a cryptographic mystery.


 2. The Eight Puzzle Chambers

Design eight distinct, interconnected levels. Each puzzle must have a definite correct answer, a working validation system, and a meaningful contribution to the final password.

 Chamber 1 — The Riddle Gate

Present a short original riddle:

“I speak without a mouth, repeat what I hear, and disappear when silence takes over. What am I?”

Answer: ECHO.

Mechanics:
- The player types an answer.
- Answers are checked without being case-sensitive.
- A correct answer unlocks the next chamber and reveals the first password fragment: ECHO.
- A hint becomes available if the player is stuck.
the hint is - You might hear me in a mountain valley or an empty tunnel when you shout something.


 Chamber 2 — The Number Cipher

Display a coded sequence:

`2 – 18 – 1 – 9 - 14'

Give the player the clue: “A is 1, B is 2, and every number represents a letter.”

The decoded answer is BRAIN

Mechanics:
- Players decode the sequence using the alphabet-number mapping.
- A correct answer reveals the fragment `BRAIN`.
- Include an interactive alphabet reference for assistance.
- provide hint to player when clicked on the hint button
Hint- “A is 1, B is 2, C is 3, and every number represents a letter.”

 Chamber 3 — The Pattern Room

Present the sequence:

2, 5, 10, 17, ?

Ask the player to identify the next number.

Correct answer: 26

the pattern is: \(n^2+1\).

Mechanics:
- Explain nothing immediately; let the player discover the pattern.
- After repeated incorrect attempts, provide a progressive hint.
- Correct completion reveals the rule: “The final password must contain at least 12 characters.”
Hint: Look at the numbers you get when you multiply a number by itself, then add 1.

 Chamber 4 — The Logic Chamber

Present three boxes labelled A, B, and C. Exactly one contains a coin.

Display these clues:
- Box A says: “The coin is in B.”
- Box B says: “The coin is not in B.”
- Box C says: “The coin is not in A.”
Rule: Exactly two statements are true.

The player must determine which box contains the coin.
answer is box C
Mechanics:
- Let players select a box.
- Validate the choice using the truth conditions.
- Reveal the next password requirement: “Include at least one uppercase letter.”

 Chamber 5 — The Symbol Lock

Show a sequence of symbols with a missing symbol. Ask the player to identify the missing symbol from four options.

Create a clear, consistent visual pattern that can be solved through observation rather than random guessing.

Mechanics:
- Use interactive symbol choices.
- Validate the selected answer.
- Reveal the requirement: “Include at least one symbol.”
- Display the allowed symbols for the game password.

 Chamber 6 — The Hidden Message

Present an encrypted message using a Caesar cipher. Give the player the shift value and ask them to decode the message.

Use a deterministic message and verify its answer in code. The decoded message should reveal a specific character or word needed to assemble the final password.

Mechanics:
- Provide an optional hint explaining how letter shifting works.
- Show immediate right/wrong feedback.
- Unlock the next chamber when the message is decoded correctly.

 Chamber 7 — The Rule Detective

Present a collection of candidate passwords and clues about their properties. The player must deduce which candidate satisfies the stated conditions.

For example, the candidate must:
- Have at least 12 characters.
- Contain an uppercase letter.
- Contain a symbol.
- Contain a riddle answer discovered earlier.

Make sure the candidate set has exactly one correct solution.

Mechanics:
- Let players inspect each candidate.
- Explain which conditions eliminate incorrect candidates.
- Reveal the rule: “Your game password cannot match any of your previous five game passwords.”

 Chamber 8 — The Final Assembly

Bring together all the password fragments, decoded clues, and discovered rules.

Display the fragments collected during previous chambers and allow the player to assemble them into a candidate password.

Mechanics:
- Provide an editable password input.
- Display a live checklist of all password requirements.
- Show which requirements pass and which fail as the player types.
- Allow the player to submit the password only when the required conditions are satisfied.
- Validate the complete answer against the game's actual solution.
- Unlock the vault only when the exact intended password is entered.

Do not accept a password merely because it satisfies the general rules. It must also match the puzzle's intended solution.

 3. Password Validation Engine

Implement a central password-validation function that checks at least these eight rules:

1. The password contains at least 12 characters.
2. It contains at least one uppercase letter.
3. It contains at least one permitted symbol.
4. It contains the required riddle answer.
5. It contains the required decoded fragment.
6. It follows the ordering or arrangement clue discovered in the puzzles.
7. It does not match any of the last five fictional game passwords.
8. It satisfies the final cipher or assembly clue.

The exact target password must be consistent with all eight rules. Ensure the clues and target password are designed together so that no puzzle gives contradictory information.

Every rule must be checked in real time. Use green check indicators for passed rules and neutral or red indicators for failed rules. Include text labels so the feedback remains accessible without relying on colour alone.

Keep the game requirements separate from real-world password-security requirements.

 4. Game Design and Interface

Build a polished, responsive browser interface with the following screens:

**Start screen**
- Game title: THE CIPHER VAULT.
- A short story introducing the mystery.
- A Start Game button.
- A clear notice that the password is fictional and must not be a real password.

**Puzzle dashboard**
- Eight chamber cards.
- Current level and progress indicator.
- Locked, active, and completed states.
- A clue notebook that stores discovered hints and fragments during the current game.

**Puzzle screen**
- Clear puzzle instructions.
- Interactive answer controls.
- Submit Answer button.
- Immediate success and failure feedback.
- Progressive hints.
- A Continue button after successful completion.

**Final password screen**
- All discovered fragments and clues.
- Password input with show/hide functionality.
- Eight live rule indicators.
- A final submission button.
- A clear message describing any failed conditions.

**Victory screen**
- A vault-opening animation or visual effect.
- A clear “VAULT UNLOCKED” message.
- A summary of the completed chambers.
- The final game password displayed as the puzzle's solution.
- A Play Again button that starts a fresh session.

5. Technical Requirements

- Build a fully functional frontend that runs in a modern browser.
- Prefer HTML, CSS, and JavaScript, or React if the environment supports it.
- Do not require a backend, account registration, or database.
- Keep puzzle answers and game state consistent.
- Prevent locked chambers from being accessed prematurely.
- Provide meaningful error messages for invalid answers.
- Support keyboard interaction and mobile screens.
- Use local game state for progress.
- Generate a fresh, internally consistent game session when restarting.
- Ensure all buttons and controls actually work.
- Do not leave placeholder puzzles, unfinished handlers, or fake success messages.

6. Puzzle Quality Requirements

The puzzles must be original, understandable, and logically solvable.

- Every puzzle must have a verifiable answer.
- Each puzzle should teach the player something useful for the final password.
- Hints should guide the player without immediately revealing the answer.
- Difficulty should increase gradually.
- Avoid puzzles that depend on obscure trivia, arbitrary guessing, or ambiguous wording.
- Ensure the intended final password passes every validation rule.
- Ensure incorrect passwords cannot unlock the vault.
- Keep the interface responsive and feedback immediate.

 7. Final Deliverable

Deliver the complete working game, not just a plan or a mockup.

Before considering it complete, test the following:
1. All eight chambers can be completed.
2. Every puzzle accepts its correct answer and rejects incorrect answers.
3. All discovered clues and fragments persist throughout the current session.
4. Every password rule updates live.
5. The intended final password passes all requirements.
6. An incorrect final password does not unlock the vault.
7. The victory screen appears only after successful validation.
8. Restarting the game resets progress correctly.


The final result should be an original, engaging puzzle game that demonstrates both creative puzzle design and technically sound implementation. The player should feel that they have genuinely cracked a mystery rather than simply filled in a password field.

PROMPT2.
without changing the game logic or mechanics or any other aspect, just add the respective sound effects, use the wrong answer.mp3 when there is a wrong answer, winning sound track.mp3 when you win, right answer.mp3 when you get a right answer, click to next level!!!.mp3 when you go to the next level

When AI got wrong--
At level 3 the hint given was incorrect and antigravity was finding it difficult to comprehend all tasks



