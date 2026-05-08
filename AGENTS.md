# Vocabulary Repository Rules

This repository stores English vocabulary learning data.

The main data file is:

- `data/words.json`

## Data format

Each word item must contain:

- id // 唯一 ID。格式：word*学习日期*单词，例如 word_20260508_available。用于防止重复和方便检索。
  // 单词本体。只存英文单词或短语本身。
- word
  // 中文意思。尽量简洁，保留最常用含义。
- meaning
  // 词性。例如：n. 名词，v. 动词，adj. 形容词，adv. 副词，prep. 介词，conj. 连词，pron. 代词。
- partOfSpeech
  // 音标。可以为空字符串，后续再补充。
- pronunciation
  // 英文例句。要求简单、自然、实用，适合初级学习者朗读和记忆。
- sentence
  // 例句中文翻译。要准确、自然，方便理解英文句子。
- translation
  // 常用搭配。优先记录最常见、最实用的搭配。
- phrase
  // 学习日期。格式必须是 YYYY-MM-DD。
- learnDate
  // 已复习次数。新单词默认是 0。
- reviewCount
  // 上次复习日期。新单词默认是空字符串；复习后使用 YYYY-MM-DD。
- lastReviewDate

## Rules

1. Do not delete old words unless explicitly asked.
2. Do not add duplicate words.
3. If a word already exists, only fill missing fields or improve weak fields.
4. Example sentences should be short, natural, practical, and easy for a beginner to read aloud.
5. Use simple daily-life or work-related sentences.
6. New words should have reviewCount = 0.
7. New words should have lastReviewDate = "".
8. Dates must use YYYY-MM-DD.
9. Keep JSON valid and formatted.
