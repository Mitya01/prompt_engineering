# prompt_engineering

## Задание

Известно, что LLM могут выдавать различные по качеству и релевантности ответы на один и тот же вопрос в зависимости от его формулировки и дополнительных инструкций. Необходимо оптимизировать промпт для получения технических скрининговых вопросов по описанию вакансии, используя Gigachat.

Результатом решения задачи должен быть выбранный оптимальный промпт, а также отчёт с описанием подборки оптимального промпта.

## Промпт

"Представь, что ты рекрутер, который ищет кандидата на позицию [название позиции], при этом кандидат должен подходить по требованиям, представленным в описании вакансии Сформулируй 5 технических скрининговых вопросов, основываясь на описании вакансии и примерах 5 скрининговых вопросов для разработчика на языке программирования Python. Вопросы должны быть краткими, понятными и соответствовать уровню знаний, необходимому для выполнения работы. При этом избегай вопросов, связанных только с личным опытом работы с конкретными инструментами или технологиями из описания вакансии. Пример такого вопроса: "Расскажите о вашем опыте работы с {название какого-нибудь инструмента, навыка который был в обязанностях или требованиях к вакансии}". Убедись, что скрининговые вопросы затрагивают несколько обязанностей и требований, предъявляемых кандидату. 

Описание вакансии: 

[Вставить описание вакансии] 

Выведи ответ в таком же формате, как и в примере ниже (выведи только вопросы, без пояснения):
Пример 5 скрининговых вопросов для разработчика на языке программирования Python. 

1. Что такое Python и перечислите некоторые из его ключевых функций. 

2. Что такое cписки и кортежи в Python? 

3. В чём разница между изменяемым типом данных и неизменяемым типом данных? 

4. Можете ли вы объяснить распространённые обхода графов в Python? 

5. Что такое ошибка KeyError в Python и как с этим справиться?

## Отчет с описанием подборки оптимального промпта.

### 1. Критерии оценки качества ответов 

Для оценки качества полученных ответов на основе промпта можно использовать следующие критерии: 

- Соответствие описанию вакансии: вопросы должны быть релевантны требованиям и обязанностям, указанным в описании вакансии. 

- Краткость и понятность: вопросы должны быть лаконичными, чтобы на них можно было устно ответить в течение короткого времени. 

- Техническая сложность: вопросы должны соответствовать уровню знаний, необходимому для выполнения работы, указанной в вакансии. 

- Единый формат вывода: все вопросы должны выводиться в одинаковом формате.

- Разнообразие вопросов: наличие различных типов вопросов для более полного скрининга кандидата. 

### 2. Проверяемые гипотезы 

- Гипотеза 1 по критерию "соответствие описанию вакансии": использование контекста о роли рекрутера может помочь в исключении вопросов, не соответствующих описанию вакансии. Например, "Представь, что ты рекрутер, который ищет кандидата на позицию [название позиции], при этом кандидат должен подходить по требованиям, представленным в описании вакансии". 

- Гипотеза 2 по критериям "краткость и понятность" и "техническая сложность": уточнение уровня сложности вопросов и того, что вопросы должны быть лаконичными, может привести к более релевантным ответам. Например, "Вопросы должны быть краткими, понятными и соответствовать уровню знаний, необходимому для выполнения работы".

- Гипотеза 3 по критерию "единый формат вывода": добавление примера, в котором представлен ожидаемый формат вывода, может помочь выводить все вопросы в одинаковом формате. Например, "Выведи ответ в таком же формате, как и в примере. <Пример>".

- Гипотеза 4 по критерию "разнообразие вопросов": добавление в промпт информации о том, что вопросы должны быть разнообразными, может улучшить качество вопросов. Например, "Убедись, что скрининговые вопросы затрагивают несколько обязанностей и требований, предъявляемых кандидату".

### 3. Оценка применения гипотез по выделенным критериям 

- Гипотеза 1 по критерию "соответствие описанию вакансии": применение контекста рекрутера привело к более целенаправленным вопросам, которые соответствуют описанию вакансии. Вопросы стали более практическими и ориентированными на кандидата. 

- Гипотеза 2 по критериям "краткость и понятность" и "техническая сложность": уточнение уровня сложности вопросов и их лаконичности позволило получить более краткие и соответствующие уровню кандидата вопросы. 

- Гипотеза 3 по критерию "единый формат вывода": пример помог выводить все вопросы в едином формате. 

- Гипотеза 4 по критерию "разнообразие вопросов": добавление в промпт информации о том, что вопросы должны быть разнообразными помогло расширить спектр проверяемых знаний кандидата.
