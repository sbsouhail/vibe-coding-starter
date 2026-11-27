# Prompts

## The formula: WHO · WHAT · HOW · LOOK

| Part | Question to answer | Example |
| --- | --- | --- |
| WHO | Who uses the app? | University students |
| WHAT | What problem, which main features? | Paste notes, get a quiz, see the score |
| HOW | What does the AI do inside the app? Any rules? | Writes 10 questions with short explanations |
| LOOK | Design, tone, languages, web or mobile? | Clean, friendly, French and English |

### Vague vs clear

Vague (many prompts wasted fixing it):

```
make a study app
```

Clear (a usable first version in one try):

```
Build a web app called StudyBuddy for university students. They paste their course notes, and the AI creates a 10-question multiple-choice quiz using only facts from the notes, with a short explanation for each answer. Show the score at the end. Clean, friendly, mobile-friendly design, in French and English.
```

### Your turn: fill in the blanks

```
Build a [web / mobile] app for [WHO]. They [what they do in the app], and the AI [what the AI does, with any rules]. [Main features]. [Design, tone and languages].
```

## When it breaks

| Situation | Prompt |
| --- | --- |
| An error appears | `Here's the error: [paste it]. Fix only this.` |
| You don't understand a part | `Explain this part of the code in simple words.` |
| The AI changes too much | `Only fix [one thing]. Change nothing else.` |
| A change made things worse | Restore the last working version from the tool's history or from GitHub, then retry in smaller steps. |
| The build fails (AI Studio) | `Fix any build issues with the current code.` |

The formula works beyond apps too: emails, reports, study plans. Any time you ask an AI for something.
