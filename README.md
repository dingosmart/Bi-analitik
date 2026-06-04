### Bi-analitik 

🇷🇺 Russian Version (Русский)
🚀 Как выжать максимум из LLM в аналитике данных: от «сделай мне красиво» к четким метрикам

Многие до сих пор воспринимают генеративный ИИ как продвинутый поисковик или текстовый редактор. Но если ваша цель — автоматизация аналитики и работа со сложными предметными областями (например, морской логистикой), базовые запросы «в лоб» превращаются в генерацию информационного шума.

Недавно в рамках программы «Аналитика больших данных» в СПбГЭУ я провел небольшой эксперимент по базовому промтинг-инжинирингу, и цифры говорят сами за себя.

📊 Что показал мини-аудит (на цифрах):

Инвестиции в запрос окупаются: Средняя длина моего простого запроса составляла всего 58 символов, а структурированного — 294 символа. Да, четкий промт в 5 раз длиннее, но...

ИИ перестает «лить воду»: В ответ на простые запросы нейросеть генерировала тонны текста (в среднем 2710 символов). Структурированный промт сократил этот объем до 1716 символов лаконичного, применимого контента.

Эффективность генерации: В итоговых отчетах доля полезного текста от ИИ составила более 90%. Но управлял этим процессом человек, задавая жесткие рамки: от выгрузки портовой статистики UNCTAD в Markdown-таблицы до строгого форматирования списков литературы по ГОСТу.

💡 Главный вывод: Эффективность работы с ИИ — это не про «угадывание» слов, а про проектирование контекста. Хотите на выходе чистый JSON с аномалиями в грузообороте портов вместо общих рассуждений? Задавайте жесткую структуру, роли и ограничения на старте.

Для ИТ-решений в сфере логистики (проект mainru.com) такой подход — это единственный способ заставить языковые модели работать как надежный инженерный инструмент, а не как непредсказуемый собеседник.

Коллеги, а как вы боретесь с «галлюцинациями» и лишним шумом в ответах LLM? Используете готовые фреймворки или полагаетесь на интуицию? 👇

#BigData #DataAnalytics #AI #PromptEngineering #DataScience #Logistics #СПбГЭУ #GitHub

🇬🇧 English Version (Английский)
🚀 Maximizing LLM Efficiency in Data Analytics: Moving from "Make it Nice" to Clear Metrics

Many still view generative AI as an advanced search engine or a text editor. However, if your goal is to automate analytics and tackle complex domains like maritime logistics, vague prompt-engineering results in nothing but information noise.

As part of the "Big Data Analytics" program at SPbGEU, I recently conducted a mini-experiment on basic prompting, and the data speaks for itself.

📊 What the Mini-Audit Revealed (by the numbers):

Investing in the prompt pays off: The average length of my basic prompt was just 58 characters, while the structured one was 294 characters. Yes, a well-defined prompt is 5 times longer, but...

The AI stops "wasting words": In response to vague prompts, the LLM generated massive walls of text (averaging 2,710 characters). A structured prompt cut this volume down to 1,716 characters of concise, actionable content.

Generation efficiency: In the final reports, the share of useful AI-generated text was over 90%. However, the process was entirely human-driven, enforcing strict constraints: from exporting UNCTAD port stats into Markdown tables to formatting bibliographies strictly according to state standards.

💡 Key Takeaway:
Efficiency with AI isn't about "guessing" the right words; it’s about context engineering. Want a clean JSON output showing port cargo turnover anomalies instead of generic essays? Define a rigid structure, roles, and boundaries right from the start.

For IT solutions in logistics (such as the mainru.com project), this approach is the only way to turn language models into reliable engineering tools rather than unpredictable conversationalists.

How do you tackle LLM hallucinations and information noise in your workflow? Do you rely on established frameworks or intuition? 👇

#BigData #DataAnalytics #AI #PromptEngineering #DataScience #Logistics #SPbGEU #GitHub

🇨🇳 Chinese Version (Китайский)
🚀 如何在大数据分析中最大化 LLM 的效率：从“模糊指令”到精准度量

许多人仍将生成式人工智能仅仅视为一个高级搜索引擎或文本编辑器。但是，如果你的目标是实现分析自动化，并处理航运物流等复杂的专业领域，那么模糊的“盲目提问”最终只会带来大量的“信息噪音”。

最近，作为 圣彼得堡国立经济大学（SPbGEU）“大数据分析”项目 的一部分，我针对基础提示词（Prompting）进行了一次微型实验，数据结果非常直观。

📊 微型审计的数据揭示：

精确提问的投入是值得的： 我的普通提示词平均只有 58 个字符，而结构化提示词则达到了 294 个字符。是的，清晰的提示词长度增加了 5 倍，但是……

AI 不再“说废话”： 面对模糊的提问，大模型生成了密密麻麻的文本（平均 2710 个字符）。而结构化的提示词将这一体积压缩到了 1716 个字符，内容极其精炼且具有实用价值。

高效的内容生成： 在最终的报告中，AI 生成的有效文本占比超过了 90%。但这一过程完全由人主导并设定了严格的框架：从将 UNCTAD（联合国贸发会议）的港口吞吐量数据转化为 Markdown 表格，到严格按照国家标准排版参考文献。

💡 核心结论：
与 AI 协作的高效核心不在于“猜词”，而在于上下文工程（Context Engineering）。如果你希望获得一个包含港口吞吐量异常分析的干净 JSON 格式输出，而不是泛泛而谈的宏观论述，那么请在最开始就制定严格的结构、角色和限制条件。

对于物流领域的 IT 解决方案（如 mainru.com 项目）而言，这种方法是让语言模型成为可靠工程工具、避免其流于“不可控聊天”的唯一途径。

各位同行，你们在实际工作中是如何应对 LLM 的“幻觉”和信息噪音的？你们是依赖成熟的框架，还是凭直觉调整？ 👇

#大数据 #数据分析 #人工智能 #提示词工程 #数据科学 #物流 #SPbGEU #GitHub



# Bi-analitik
Practical Work No. 1 for the course «Big Data Analytics» (Saint Petersburg State University of Economics / SPbGEU). Basic Prompting: Data Collection on Maritime Logistics and Visualization of LLM Performance Metrics
# Модуль: Базовый промтинг в аналитике данных (Морская логистика)

Репозиторий содержит материалы практической работы в рамках программы профессиональной переподготовки **«Аналитика больших данных» (СПбГЭУ)**.

## 🎯 Цель проекта
Демонстрация перехода от интуитивного (хаотичного) взаимодействия с большими языковыми моделями (LLM) к инженерному подходу проектирования контекста. В качестве предметной области выбрана аналитика морской логистики и портовой инфраструктуры.

## 📁 Содержимое репозитория
* `practice_1_prompting.ipynb` — Jupyter-ноутбук с выполненными заданиями, включая:
  * Сбор и структурирование данных по крупнейшим мировым портам (на базе отчетов UNCTAD).
  * Выявление аномалий в грузообороте и выгрузка данных в формате JSON.
  * Форматирование списков литературы по ГОСТ Р 7.0.100–2018.
* `scripts/` — Python-скрипты на базе `matplotlib` и `numpy` для генерации аналитических графиков.
* `images/` — графики метрик эффективности (соотношение длин запросов/ответов, объем полезной генерации).

## 📊 Ключевые результаты мини-аудита
В ходе работы было проведено сравнение простых и структурированных запросов к ИИ. Метрики показали, что детальное проектирование промпта (увеличение длины запроса в среднем в 5 раз) снижает объем "информационного шума" в ответах ИИ на 36%, повышая плотность и лаконичность полезных данных.

---
*Выполнено: Пономарев Алексей, 2026 г.*
