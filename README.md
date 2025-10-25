# Лабораторный проект: EDA (Diabetes Dataset)

## Цель
Командный пошаговый анализ данных (EDA) + подготовка датафрейма для последующего моделирования.

## Участники и файлы
| Участник | Роль | Ноутбук |
|----------|------|---------|
| Роман | Импорт и диагностика | 01_import_diagnostics.ipynb |
| Илья | Описательная статистика | 02_univariate.ipynb |
| Максим | Двухфакторный анализ и корреляции | 03_bivariate_corr.ipynb |
| Стас | Подготовка данных (импутация, кодирование, масштабирование) | 04_preprocessing.ipynb |
| Кирилл | Выбросы и итоговые выводы | 05_outliers_conclusions.ipynb |

## Структура проекта
```
notebooks/        — отдельный ноутбук под каждый этап  
data/raw/         — исходные данные (diabetes.csv)  
data/interim/     — промежуточные (например, diabetes_stage1.csv)  
data/processed/   — финальные данные для моделирования  
src/              — вспомогательные функции (опционально)  
```

## Быстрый старт
```bash
git clone https://github.com/Soloda1/diabetes-eda-lab.git
cd diabetes-eda-lab
pip install -r requirements.txt
# Положить diabetes.csv в data/raw/
jupyter lab  # или jupyter notebook
```

## Правила Git (минимум)
1. Каждый редактирует ТОЛЬКО свой ноутбук.  
2. Перед push: `git pull --rebase`.  
3. Сообщения коммитов короткие: `feat: add univariate plots` или `fix: update missing logic`.  
4. Не коммитим большие сырые данные > 50МБ.  
5. Если нужно добавить библиотеку → добавь её в requirements.txt.

## Мини Git-шпаргалка
```bash
git status
git add notebooks/02_univariate.ipynb
git commit -m "feat: univariate initial"
git pull --rebase
git push
```

## Данные
Источник: Pima Indians Diabetes (UCI / Kaggle).  
Файл: `data/raw/diabetes.csv`.  
Нули в Glucose, BloodPressure, SkinThickness, Insulin, BMI → скрытые пропуски.

## Дальнейшие шаги
- После завершения всех этапов можно объединить выводы в один отчёт (PDF/Markdown).
