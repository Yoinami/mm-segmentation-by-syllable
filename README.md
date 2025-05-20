# Myanmar Syllable Segmentation
This project provides a Python function to segment Myanmar text into syllables or characters, handling various edge cases specific to the Myanmar script. It is designed to distinguish between similar-looking characters (such as ၀ (zero) and ဝ (wa)), handle consonant clusters, vowels, medials, digits, punctuation, and even English text within Myanmar sentences.

## Features
- Segments Myanmar text into syllables/characters using regular expressions.
- Optionally treats ၀ (zero) and ဝ (wa) as the same character.
- Handles Myanmar consonants, vowels, medials, digits, punctuation, and English text.
- Designed to accommodate common user input misalignments and edge cases.
## Usage
```python
from mmsegmentation import segment_characters

text = "ကိစ္စ ၀တ္ထု"
result = segment_characters(text)
print(result)
```
Command Line Example
You can run the script directly to test the segmentation

```python
from mmsegmentation import segment_characters

segment_characters(string)
```
You can also use it by importing the function

## Function Reference
``
segment_characters(text: str, include_zero: bool = False) -> list[str]``
Segments Myanmar input text into characters/syllables.

- text: Input Myanmar string.
- include_zero: If True, treats ၀ (zero) and ဝ (wa) as the same character.
Returns a list of segmented syllables/characters.

Notes
The segmentation logic is based on regular expressions tailored for Myanmar script.
Some edge cases and complex rules (e.g., for words like ``မားစ်ဂြိုလ် -> [မားစ်, ဂြိုလ်]`` and ``၀တ္ထု -> [၀တ္ထု]``) may require further refinement.
The code is a work in progress and may need additional testing for rare or complex input cases.