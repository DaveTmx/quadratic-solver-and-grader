
# Quadratic Solver and Grading System

A single-file web application (`index.html`) with two tools: a **Quadratic Equation Solver** and a **Grading System** calculator. Built with HTML, CSS and JavaScript, with no external libraries. Runs entirely offline.

Developed for ICT251 (JS GitHub Activity).

## How to Run

Open `index.html` in any modern web browser. No installation or internet connection is needed.

## Tools

### 1. Quadratic Solver

Solves equations of the form **ax² + bx + c = 0**. For any valid input, it:
- Calculates the discriminant, Δ = b² − 4ac
- Identifies the nature of the roots: two distinct real roots, one repeated real root, or two complex conjugate roots
- Displays the roots, rounded to three decimal places

**Validation:** Rejects empty or non-numeric inputs, and rejects a = 0.

### 2. Grading System

Converts a score from 0 to 100 into a letter grade.

**Grade bands:**

| Grade | Score range |
|---|---|
| A+ | 85 – 100 |
| A | 75 – 84 |
| B+ | 65 – 74 |
| B | 60 – 64 |
| C+ | 55 – 59 |
| C | 50 – 54 |
| D | 0 – 49 |

**Validation:** Rejects empty input, and rejects scores below 0 or above 100.

## Test Cases

### Quadratic Solver

| a | b | c | Discriminant | Nature of roots | Expected output |
|---|---|---|---|---|---|
| 1 | -3 | 2 | 1.000 | Two distinct real roots | x₁ = 2.000, x₂ = 1.000 |
| 1 | -4 | 4 | 0.000 | One real repeated root | x = 2.000 |
| 1 | 2 | 5 | -16.000 | Two complex conjugate roots | x₁ = -1.000 + 2.000i, x₂ = -1.000 - 2.000i |
| 2 | 0 | -8 | 64.000 | Two distinct real roots | x₁ = 2.000, x₂ = -2.000 |
| 1 | 0 | 0 | 0.000 | One real repeated root | x = 0.000 |
| 0 | 5 | 1 | N/A | Error | `Error: a cannot be zero for a quadratic equation.` |
| (blank) | 5 | 1 | N/A | Error | `Error: All inputs must be valid numbers.` |

### Grading System

| Score | Expected grade | Reason |
|---|---|---|
| 100 | A+ | Upper bound |
| 85 | A+ | Lower bound of A+ |
| 84 | A | Just below A+ |
| 75 | A | Lower bound of A |
| 74 | B+ | Just below A |
| 65 | B+ | Lower bound of B+ |
| 64 | B | Just below B+ |
| 60 | B | Lower bound of B |
| 59 | C+ | Just below B |
| 55 | C+ | Lower bound of C+ |
| 54 | C | Just below C+ |
| 50 | C | Lower bound of C |
| 49 | D | Just below C |
| 0 | D | Lower bound |
| -5 | Error: `Error: Score must be between 0 and 100.` | Below range |
| 101 | Error: `Error: Score must be between 0 and 100.` | Above range |
| (blank) | Error: `Error: Score cannot be empty.` | No input |

## Project Structure
├── index.html    # Complete application (HTML, CSS and JavaScript)
└── README.md     # This file

## Author

David Kanyama ([@DaveTmx](https://github.com/DaveTmx))

