# Palindrome Checker

[![PyPI Version](https://img.shields.io/pypi/v/palindrome_checker)](https://pypi.org/project/palindrome_checker/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Versions](https://img.shields.io/pypi/pyversions/palindrome_checker)](https://pypi.org/project/palindrome_checker/)

A Python package to check if a string (or integer) is a palindrome, ignoring case, punctuation, and non-alphanumeric characters.

## Features

- ✅ **Robust Handling**: Works with:
  - Mixed case (`"RaceCar"`)
  - Punctuation (`"Madam, I'm Adam."`)
  - Integers (`12321`)
- 🛠 **Extensible**: Use the `Phrase` class directly for custom processing.
- 🧪 **Tested**: 100% test coverage with pytest.

## Installation

```bash
pip install palindrome_checker
```

## Basic Usage

```python
from palindrome_checker import is_palindrome

# Simple detection
print(is_palindrome("A man, a plan, a canal, Panama!"))  # True
print(is_palindrome("Not a palindrome"))  # False

# Works with numbers too!
print(is_palindrome(12321))  # True
```

## Advance Usage

```python
from palindrome_checker.phrase import Phrase

phrase = Phrase("RaceCar")
print(phrase.ispalindrome())  # True

# See processed content (cleaned version used for checking)
print(phrase.processed_content())  # "racecar"

# Get just alphanumeric characters
print(phrase.letters_and_digits())  # "RaceCar"
```

## Development

### Setup
1. Clone repo:
   ```bash
   git clone https://github.com/yourusername/palindrome_checker.git
   cd palindrome_checker
   ```
2. Install with dev dependencies:
   ```bash
   pip install -e .
   ```
### Running Tests
```bash
pytest
```

## Contact
Faizan Awnar - @thefaizananwar - faizanunique5@gmail.com
