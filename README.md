#  Agile Estimation (Planning Poker vs AI)


## Description
The Lab 3 backlog of the Campus Event Management System was estimated
in story points (Fibonacci scale 1, 2, 3, 5, 8, 13) by three team members
in a blind Planning Poker round and by an AI assistant as a fourth voice.
The gaps between them were then analysed and used to plan a sprint.

## How to Run
```
python "Lab 4 Sheeza (SP24-BSE-43).py"
```
No extra libraries are needed. Expected output:
- a comparison table (ID, Story, members A/B/C, Team, AI, Diff)
- the spread (min to max) of the three member estimates for each story
- `AI reasons that were assumed, not known: 4 ['S4', 'S6', 'S7', 'S10']`
- `Three biggest gaps: ['S4', 'S6', 'S7']`
- `Total backlog points: 42`
- `Fits in sprint 1: ['S1', 'S2', 'S3', 'S4', 'S5'] = 19 points out of 20`

## What I Did
1. **AI estimates:** the AI sized every story on the Fibonacci scale and
   gave one line on the main source of complexity.
2. **Planning Poker:** each member wrote estimates privately before anyone
   spoke, then all were revealed and discussed until the team agreed.
3. **Comparison table:** the AI and the team matched on simple stories
   (login, browse) and differed most on stories that depend on unsettled
   things (registration, reminders).
4. **Sprint planning:** stories were taken in priority order until the
   velocity limit was reached.

## Blind Estimates (Task 1)
The spread of A, B and C is kept for every story because the
disagreement is the data. The widest spread is S6 Reminders (8 to 13).
The code asserts that every estimate is on the Fibonacci scale.

## Auditing the AI (Task 2)
For each story, was the AI's reason known from the backlog text, or
assumed? In 4 stories the reason was assumed: S4, S6, S7, S10.

## Three Biggest Gaps (Task 3)
| Story | Team | AI | What the AI could not know |
|-------|------|----|----------------------------|
| S4 Register | 8 | 5 | our event-capacity schema is not finalised |
| S6 Reminders | 8 | 5 | no notification service yet, nobody has used a scheduler |
| S7 Search | 5 | 3 | event table has no indexes, categories are free text |

## Sprint Capacity (Task 4)
- Assumed velocity: 20 points for a two-week sprint (a starting guess
  for a new team).
- Sprint 1: S1 + S2 + S3 + S4 + S5 = 3 + 2 + 3 + 8 + 3 = **19 points**.
- S6 (8 points) would make 27, which is over 20, so it moves to sprint 2.
- Full backlog = 42 points, which is more than two sprints at this velocity.
- Confidence: expected error is about 30% because the team is new. After
  the sprint, the points actually completed will replace the guessed velocity.

## Evidence
- Commit history: `<paste output of git log --oneline>`
- Program output: `<paste screenshot of the terminal output>`
- Team's real blind estimates: `<replace the sample data with your group's numbers>`







<img width="726" height="317" alt="LAB4(1)" src="https://github.com/user-attachments/assets/34ef6ab3-34b9-421d-ba06-1b17d8080af4" />

<img width="667" height="267" alt="LAB4(2)" src="https://github.com/user-attachments/assets/f2818088-c18a-45ce-bc3c-89fbb6527976" />

<img width="666" height="262" alt="LAB4(3)" src="https://github.com/user-attachments/assets/183395d9-b1c6-4a1b-acb5-d7689c46c77d" />



