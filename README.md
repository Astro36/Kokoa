# KokoaNLP

> Unsupervised Learning Korean Kernel Object Analyzer

[![npm](https://img.shields.io/npm/v/kokoanlp.svg?style=for-the-badge)](https://www.npmjs.com/package/kokoanlp) [![npm](https://img.shields.io/npm/dt/kokoanlp.svg?style=for-the-badge)](https://www.npmjs.com/package/kokoanlp)

KokoaNLP는 “Korean Kernel Object Analyzer Natural Language Processor”의 약자로 **비지도 학습 기반의 한국어 자연어 처리 도구**입니다. 간결함과 실용성을 지향하는 KokoaNLP는 단어 추출, 어절 분석, 키워드 추출, 띄어쓰기 교정 등의 한국어 문서 처리에 필요한 기능을 지원합니다.

KokoaNLP의 단어 추출 알고리즘은 [Hyunjoong Kim](https://github.com/lovit)님의 [soynlp](https://github.com/lovit/soynlp)에서 아이디어를 얻어 제작되었습니다.

## ChangeLog

See [CHANGELOG](./CHANGELOG.md)

## Demo

![Demo Screenshot](./demo/images/screenshot.png)

See [Demo](https://astro36.github.io/Kokoa/demo/index.html)

## Features

- Train your own model.
- Extract words from the document.
- Find keywords and keysentences from the document.
- Fix space on the sentences.

## Installation

- Install with npm:

```bash
npm install kokoanlp --save
```

- Clone the repo:

```bash
git clone https://github.com/Astro36/Kokoa.git
```

## Usage

### API Documentation

See [API](http://astro36.github.io/Kokoa/api/index.html)

### Example

Extract words from the given document:

```javascript
const Kokoa = require('kokoanlp');
const kokoa = Kokoa.load('./data/kokoa.*.csv');
const words = kokoa.words('태평양 전쟁 개전 당시 일본 해군의 전략은 외곽 방어망 곳곳에 배치된 지상비행장이 방어의 근거지가 되고 유사시 적을 방어선 가까이 끌어들이는 동안 항공기를 집결하여 격퇴하는 것이었다.');
console.log(words); // ['태평양', '전쟁', '개전', '당시', '일본', '해군', '전략', '외곽', '방어', '곳곳에', '배치', '방어', '되고', '방어', '가까이', '동안', '항공', '것이']
```

## License

```text
KokoaNLP
Copyright (C) 2018  Seungjae Park

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```

KokoaNLP is licensed under the [GPL 3.0](./LICENSE).

[Materialize](http://materializecss.com/) is licensed under a [MIT License](https://github.com/Dogfalo/materialize/blob/master/LICENSE) by Dogfalo.
