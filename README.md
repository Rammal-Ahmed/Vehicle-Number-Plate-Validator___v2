<div align="center">

# 🚗 Number Plate Validator

**A small Python tool that checks whether a vehicle number plate follows the `ABC-123` format.**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat&logo=python&logoColor=white)
![Type](https://img.shields.io/badge/Type-CLI-2E3440?style=flat)
![Level](https://img.shields.io/badge/Level-Beginner-8FBCBB?style=flat)
![Version](https://img.shields.io/badge/Version-2-A3BE8C?style=flat)

</div>

---

## 📖 About

This project came out of my Python practice, where I was working on string methods and conditional logic. The idea is simple: you type a number plate, and the program tells you whether it is valid. If it is not, it tells you exactly which rule it broke, so the message is actually useful.

Version 2 tightens the checks and fixes two issues from my first attempt: the capital-letter check now covers all 3 letters, and short inputs no longer crash the program.

## 📋 The Format

```
  A B C - 1 2 3
  └─┬─┘ │ └─┬─┘
    │   │   └── 3 digits
    │   └────── hyphen
    └────────── 3 capital letters
```

| Rule | Requirement |
|------|-------------|
| Length | Exactly 7 characters |
| Letters | First 3 characters are alphabets |
| Case | Those letters are capitalized |
| Separator | 4th character is a hyphen (`-`) |
| Digits | Last 3 characters are numbers |

## ⚙️ How It Works

The input goes through the rules above in order and stops at the first one that fails. Checking the length first keeps the program safe from short inputs, since the later checks look at fixed positions in the text.

Methods used: `strip()`, `len()`, `isalpha()`, `isupper()`, `isdigit()` and string slicing.

## 🚀 Getting Started

**Requirements:** Python 3.x

```bash
# clone the repository
git clone https://github.com/Rammal-Ahmed/number-plate-validator.git

# move into the folder
cd number-plate-validator

# run it
python number_plate_validator.py
```

## 🖥️ Sample Runs

**Valid plate**
```
Enter your number plate: ABC-123
Valid plate: ABC-123 (format accepted)
```

**Invalid plate**
```
Enter your number plate: abc-123
Invalid: letters must be capitalized
```

## 🧪 Test Cases

| Input | Result |
|-------|--------|
| `ABC-123` | Valid plate |
| `abc-123` | Letters must be capitalized |
| `AB1-123` | First 3 characters must be letters |
| `ABC123` | Expected 7 characters, got 6 |
| `ABC_123` | A hyphen is required after the letters |
| `ABCD-12` | A hyphen is required after the letters |
| `ABC-12A` | Last 3 characters must be digits |

## 📁 Project Structure

```
number-plate-validator/
├── number_plate_validator.py
└── README.md
```

## 🎯 What I Practiced

- Chaining conditions with `if / elif / else`
- Validating text with built-in string methods
- Slicing strings by position
- Writing error messages that tell the user what to fix
- Thinking about edge cases, like very short input

## 🔮 Ideas for Next Time

- [ ] Keep asking until a valid plate is entered
- [ ] Accept more than one plate format
- [ ] Wrap the checks in a reusable function
- [ ] Add a few automated tests

## 🤝 Feedback

Suggestions and improvements are always welcome. Feel free to open an issue or fork the repo.

---

<div align="center">

**BUILT FOR THE COMMUNITY, HOPE IT HELPS**

*See you in the next repositories..!*

</div>


## About me

# **Rammal Ahmed**

**AI & Data Science Enthusiast** | **Microsoft Dynamics 365 CRM Developer** | **Power Platform** | **UI/UX Designer** | **Graphic Designer & Illustrator**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/rammal-ahmed-58184b325)
[![GitHub](https://img.shields.io/badge/GitHub-Rammal--Ahmed-181717?style=flat&logo=github)](https://github.com/Rammal-Ahmed)

<div align="center">

If you found this useful, consider giving it a star ⭐

**I truly value your feedback and welcome any suggestions for improvement**

**Always open to fresh perspectives, constructive feedback, and new ideas**


## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details

---

*Developed as part of my Python programming practice*

---

**Project Status:** Completed

</div>
