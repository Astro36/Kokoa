# Data

## New Crawler

- [뉴스 기사 크롤러](./news_crawler.py)

### Requirements

- Python 2.7
  - bs4
  - requests

### Example

Crawl 조선일보 articles:

```bash
python news_crawler.py --type 조선일보 --start-id 0003369060
```

## Prebuilt Data

- [words.7z](./words.7z)

Unzip `words.7z` as CSV file.

You can use the prebuilt model with [Kokoa.loadFile(file)](https://astro36.github.io/Kokoa/Kokoa.html#.loadFile) function:

```javascript
const Kokoa = require('kokoanlp');
const kokoa = Kokoa.load('./data/words.csv');
```