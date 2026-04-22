## Khmer Normalizer 

A missing toolkit for **Khmer Natural Language Processing**.

- Character Reordering
- Duplicate Whitespaces
- Remove zero width space
- Remove emojis
- Fix Common misspellings
- Fix Unicode issues
- Fix Khmer trailing vowels
- URL Replacements
- Hashtags Replacements
- Unicode Normalization (NFKC)
- Quotes symbols normalization
- Remove repeated punctuations

### Installation

```shell
pip install khmernormalizer
```

### Usage

```python
from khmernormalizer import normalize

input_str = """
តាម៖៖​សេចក្តី​រាយ​ការណ៍​​ឲ្យ​ដឹង​ថា!!!!!
https://google.com/a?x=1
កាល 😂 ពីវេលាម៉ោង    ៗ      ប្រមាណ១១យប់ថ្ងៃទី៤ 😂😂😂😂😂 ??
កាាាាត់
មិិិិិន 
មួយរយះះះះះះះ
រយះពេល
#សួស្ដី #KhmerNLP
""".strip()

normalize(input_str, 
          emoji_replacement="", 
          remove_zwsp=True, 
          url_replacement="",
          hashtag_replacement="")
```

Result:
```
តាម៖សេចក្តីរាយការណ៍ឱ្យដឹងថា!

កាល ពីវេលាម៉ោងៗ ប្រមាណ១១យប់ថ្ងៃទី៤?
កាត់
មិន 
មួយរយៈ
រយៈពេល
```

### Reference

- [sillsdev/khmer-character-specification](https://github.com/sillsdev/khmer-character-specification)
