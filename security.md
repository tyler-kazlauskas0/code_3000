# Security Statement

## Intended Users

This repository holds my coursework for CSE 3000: Contemporary Issues in Computer Science and Engineering. The intended users are:

- **@tyler-kazlauskas**, as the student completing and submitting the assignments.
- **Course staff** (the instructor and TAs), who review and grade the work through Gradescope's GitHub connection.

The code is for teaching only. It is not meant for production use or for any real decisions about people.

## Risk Assessment

All the data in this repo is fake data made for the class. None of it is about real people, and there are no passwords or personal info in it. So the overall risk is **low**. Here is what could go wrong if someone got the code:

| Part | What it does | What could go wrong |
|------|--------------|---------------------|
| `mod02` bot predictor | Guesses if a social media account is a bot | Someone could learn what the model looks for and make bots that avoid getting caught. |
| `mod04` bias | Checks if a model is unfair to a group of people | Someone could learn how to hide unfairness in a model. |
| `mod06` de-anonymization | Matches "anonymous" records back to people's names | This is the riskiest part. If used on real data, it could reveal who people are. The names here are fake, so nobody is exposed. |
| `mod08` sustainability | Calculates energy use and pollution | Basically no risk. |
| Homework answers | My finished assignments | Other students could copy my work. This is the most likely risk. |

## Steps Taken to Secure the Repo

- **CODEOWNERS file**: This file names who is in charge of the code. That person has to approve changes.
- **Pull requests**: Changes can be made on a separate branch and then merged into `main` with a pull request, so they can be reviewed first.
- **`.gitignore`**: This file tells Git which files to leave out. My local Python environment, setup script, Python cache files (`__pycache__`), and Mac system files are not uploaded.
- **No passwords or keys**: Nothing secret is stored in the repo, and the code doesn't need any to run.
- **Fake data only**: All the data was made up for the course, so nobody's real information can leak.
- **Limited access**: Only course staff need to see the repo (through Gradescope), so other students can't copy my answers.

I don't need stronger protections, like extra rules that block pushes to `main`. This is a homework repo with no sensitive data and nothing running live, so the extra setup isn't worth it.
