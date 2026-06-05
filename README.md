### Bi-analitik 
Bi-analitik/
├── README.md                          # Главный файл (с вкладками языков)
├── LICENSE                            # MIT License
├── requirements.txt                   # Зависимости
├── Zadanie_1_Ponomariov_04_06_2026.ipynb  # Ваш ноутбук (можно расширить)
├── scripts/
│   └── plot_metrics.py                # Генерация графиков
├── images/                            # Сюда сохранятся графики
│   ├── prompt_length_vs_response.png
│   ├── useful_content_ratio.png
│   └── efficiency_comparison.png
└── prompts/                           # Новая папка с примерами промтов
    ├── bad_prompt.txt                 # Плохой промт (на трёх языках)
    ├── good_prompt.txt                # Хороший промт (на трёх языках)
    └── json_schema.json               # Схема JSON для вывода

    # 🚢 Bi-analitik / 大数据分析实践 / Big Data Analytics

> **Практическая работа №1 | СПбГЭУ | Аналитика больших данных**  
> **实践作业 №1 | 圣彼得堡国立经济大学 | 大数据分析**  
> **Practical Work No. 1 | SPbGEU | Big Data Analytics**

[![Jupyter Notebook](https://img.shields.io/badge/Notebook-.ipynb-orange)](Zadanie_1_Ponomariov_04_06_2026.ipynb)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Three Languages](https://img.shields.io/badge/lang-русский%20|%20English%20|%20中文-red)]()

---

<!-- TABS START -->
<div align="center">
  
| 🇷🇺 Русский | 🇬🇧 English | 🇨🇳 中文 |
|-------------|------------|---------|
| [Описание](#-русский) | [Description](#-english) | [项目描述](#-中文) |

</div>
<!-- TABS END -->

---

## 🇷🇺 Русский

### 📌 О проекте

Многие до сих пор общаются с GPT как с "волшебным поисковиком": написал 2 слова — получил простыню текста.  
А что, если подойти к LLM как к **инженерному инструменту**?

Этот проект — честный эксперимент на реальных данных **морской логистики** (UNCTAD, порты, грузообороты).  
Мы сравнили **хаотичные промты** vs **структурированные промты** и замерили разницу.

🎯 **Главный вопрос:**  
*Можно ли заставить нейросеть выдавать чистый JSON с аномалиями вместо "воды"?*

### 📊 Ключевые метрики (цифры не врут)

| Параметр | Простой промт | Структурированный промт | Изменение |
|----------|--------------|------------------------|-----------|
| **Длина запроса** | 58 символов | 294 символа | **+407%** |
| **Объем ответа** | 2710 символов | 1716 символов | **-37%** |
| **Доля полезного контента** | ~40% | **>90%** | **+125%** |
| **Формат вывода** | Текст + рассуждения | Markdown / JSON / ГОСТ | ✅ Контроль |

💡 **Вывод:** Инвестиции в промт окупаются. Четкий запрос длиннее в 5 раз, но ответ в 2+ раза полезнее.

### 🔍 Примеры промтов

#### ❌ Простой (хаотичный) промт
> «Собери данные по крупнейшим портам мира и найди аномалии»

**Результат:** 3 страницы "воды", цифры "из головы", нет источников.

#### ✅ Структурированный промт
```text
Ты — аналитик данных по морской логистике.

Задача:
1. Используй данные UNCTAD за 2020–2023 гг.
2. Выгрузи топ-10 портов по TEU (контейнерооборот)
3. Формат вывода: Markdown-таблица (порт, страна, TEU_2023, рост_%)
4. Если годовых данных нет — укажи "no_data"
5. Аномалии (>30% падения или роста) выведи отдельным JSON

Ограничения:
- Никаких рассуждений
- Только таблица + JSON
- Библиография по ГОСТ Р 7.0.100–2018


Как запустить
bash
git clone https://github.com/dingosmart/Bi-analitik.git
cd Bi-analitik
pip install -r requirements.txt
python scripts/plot_metrics.py  # сгенерировать графики
jupyter notebook Zadanie_1_Ponomariov_04_06_2026.ipynb

🇬🇧 English
📌 About
Many still interact with GPT as a "magic search engine": type 2 words, get pages of text.
What if we treat LLMs as an engineering tool instead?

This project is an honest experiment using real maritime logistics data (UNCTAD, ports, cargo turnover).
We compared chaotic prompts vs structured prompts and measured the difference.

🎯 Key question:
Can we force an LLM to output clean JSON with anomalies instead of "water"?

📊 Key Metrics (numbers don't lie)
Parameter	Simple prompt	Structured prompt	Change
Prompt length	58 chars	294 chars	+407%
Response volume	2710 chars	1716 chars	-37%
Useful content %	~40%	>90%	+125%
Output format	Text + rambling	Markdown / JSON / GOST	✅ Controlled
💡 Conclusion: Investing in prompts pays off. A clear prompt is 5x longer, but the response is 2x+ more useful.

🔍 Prompt Examples
❌ Simple (chaotic) prompt
"Collect data on the world's largest ports and find anomalies"

Result: 3 pages of fluff, made-up numbers, no sources.

✅ Structured prompt

You are a maritime logistics data analyst.

Task:
1. Use UNCTAD data for 2020–2023
2. Extract top-10 ports by TEU (container turnover)
3. Output format: Markdown table (port, country, TEU_2023, growth_%)
4. If annual data is missing — write "no_data"
5. Output anomalies (>30% drop or growth) as separate JSON

Constraints:
- No reasoning
- Only table + JSON
- Bibliography according to GOST R 7.0.100–2018

How to run
bash
git clone https://github.com/dingosmart/Bi-analitik.git
cd Bi-analitik
pip install -r requirements.txt
python scripts/plot_metrics.py
jupyter notebook Zadanie_1_Ponomariov_04_06_2026.ipynb

🇨🇳 中文
📌 项目描述
许多人仍然把 GPT 当作"魔法搜索引擎"：输入几个词，得到几页文字。
如果我们把 LLM 当作工程工具会怎样？

本项目基于真实的海运物流数据（UNCTAD、港口、吞吐量）进行了一场诚实的实验。
我们比较了混乱的提示词 vs 结构化的提示词，并测量了差异。

🎯 核心问题：
能否让 LLM 输出干净的 JSON（含异常检测），而不是"注水"的文本？

📊 关键指标（数据不会说谎）
参数	简单提示词	结构化提示词	变化
提示词长度	58 字符	294 字符	+407%
回复体积	2710 字符	1716 字符	-37%
有用内容占比	~40%	>90%	+125%
输出格式	文本 + 空话	Markdown / JSON / 国家标准	✅ 可控
💡 结论： 投资提示词是值得的。清晰的提示词长 5 倍，但回复有用性提高 2 倍以上。

🔍 提示词示例
❌ 简单（混乱）提示词
"收集全球主要港口的数据并找出异常"

结果： 3 页空话，编造的数字，没有来源。

✅ 结构化提示词
text
你是一名海运物流数据分析师。

任务：
1. 使用 UNCTAD 2020–2023 年数据
2. 提取前 10 大港口（按 TEU 集装箱吞吐量）
3. 输出格式：Markdown 表格（港口、国家、TEU_2023、增长率_%）
4. 如果缺少年度数据 — 填写 "no_data"
5. 将异常（降幅或增幅 >30%）输出为单独的 JSON

限制：
- 不要推理
- 只输出表格 + JSON
- 参考文献按照 ГОСТ Р 7.0.100–2018 格式

如何运行
bash
git clone https://github.com/dingosmart/Bi-analitik.git
cd Bi-analitik
pip install -r requirements.txt
python scripts/plot_metrics.py
jupyter notebook Zadanie_1_Ponomariov_04_06_2026.ipynb

💎 Главный вывод / Key Takeaway / 核心结论
Эффективность LLM — не про "угадывание слов", а про проектирование контекста.
LLM efficiency isn't about "guessing words" — it's about context engineering.
LLM 的效率不在于"猜测词语"，而在于上下文工程。

Жесткая структура, роли, форматы вывода и ограничения превращают ИИ из «болтуна» в надежный инструмент.

🙋 Вопрос сообществу / Question / 问题
Как вы боретесь с галлюцинациями LLM?
How do you tackle LLM hallucinations?
你如何应对 LLM 的幻觉问题？

Используете фреймворки (DSPy, LangChain)?

Do you use frameworks (DSPy, LangChain)?

你使用框架吗（DSPy、LangChain）？

Или полагаетесь на ручной промтинг?

Or rely on manual prompting?

还是依赖手动提示词？

Открыт к Issue и PR. Давайте делать промпт-инжиниринг инженерной дисциплиной!
Open to Issues and PRs. Let's make prompt engineering an engineering discipline!
欢迎提交 Issue 和 PR。让我们把提示词工程变成一门真正的工程学科！

📚 Источники / Sources / 来源
UNCTAD Maritime Transport Data

СПбГЭУ — Аналитика больших данных

mainru.com — логистические IT-решения

Автор / Author / 作者: Алексей Пономарев (@dingosmart)
Год / Year / 年份: 2026
Лицензия / License / 许可证: MIT


-
