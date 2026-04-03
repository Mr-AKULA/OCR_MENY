# ⚡ БЫСТРАЯ СПРАВКА - ГЛАВНОЕ

## 🎯 ВСЁ ЧТО НУЖНО (для спешки)

### 1️⃣ Получить бесплатный Groq ключ (2 мин)

```
https://console.groq.com/
→ Войти через Google
→ API Keys → Create API Key
→ Скопировать значение (gsk_xxxx...)
```

### 2️⃣ Открыть Google Colab (30 сек)

```
https://colab.research.google.com/
```

### 3️⃣ Загрузить notebook (30 сек)

```
Выберите: menu_parser_free.ipynb
```

### 4️⃣ Отредактировать БЛОК 3 (1 мин)

```python
GROQ_API_KEY = "gsk_ваш_ключ"
FIRM_ID = "70000001048209528"  # или другой
```

### 5️⃣ Загрузить фото меню (2 мин)

```
Google Drive → Menu_Parser → photos
Загрузить 1-4 фото меню
```

### 6️⃣ ЗАПУСТИТЬ (30 сек)

```python
# БЛОК 11 - нажмите ▶️
process_menu(firm_id=FIRM_ID)
```

### 7️⃣ Результаты (готово!)

```
✓ Google Drive → Menu_Parser → results
  ├── menu_...csv
  └── menu_...xml
```

---

## 🔑 КЛЮЧЕВЫЕ ССЫЛКИ

| Что нужно | Ссылка |
|-----------|--------|
| 🔐 Groq API (БЕСПЛАТНО!) | https://console.groq.com/ |
| 📓 Google Colab | https://colab.research.google.com/ |
| 📁 Google Drive | https://drive.google.com/ |
| 📍 2ГИС (найти ID) | https://2gis.ru/ |

---

## 📝 ФАЙЛЫ ЧТО Я СОЗДАЛ

| Файл | Для чего |
|------|----------|
| **menu_parser_free.ipynb** | 👈 ГЛАВНЫЙ файл (копируйте в Colab) |
| БЕСПЛАТНАЯ_ВЕРСИЯ_README.md | Подробная инструкция |
| ПОЛУЧИТЬ_GROQ_КЛЮЧ.md | Как получить API ключ |

---

## ⚙️ ГЛАВНЫЕ ПЕРЕМЕННЫЕ

```python
# БЛОК 3 - ОТРЕДАКТИРУЙТЕ:

GROQ_API_KEY = "gsk_xxxxx"              # ← Ваш ключ
FIRM_ID = "70000001048209528"          # ← ID кофейни
GOOGLE_DRIVE_FOLDER = "Menu_Parser"    # ← Папка на Drive
```

---

## 🚀 ТИПОВЫЕ КОМАНДЫ

### Обработать один ресторан
```python
process_menu(firm_id="70000001048209528")
```

### Обработать несколько
```python
for firm_id in ["ID1", "ID2", "ID3"]:
    process_menu(firm_id=firm_id)
```

### Посмотреть CSV результат
```python
import pandas as pd
csv_files = list(folders['results'].glob("*.csv"))
df = pd.read_csv(max(csv_files, key=lambda p: p.stat().st_mtime), delimiter='|')
print(df)
```

### Посмотреть XML результат
```python
xml_files = list(folders['results'].glob("*.xml"))
with open(max(xml_files, key=lambda p: p.stat().st_mtime)) as f:
    print(f.read())
```

---

## 💰 СТОИМОСТЬ

| Компонент | Цена |
|-----------|------|
| Tesseract OCR | 🆓 FREE |
| Groq LLM API | 🆓 FREE |
| Google Drive | 🆓 15GB FREE |
| Google Colab | 🆓 FREE |
| **ИТОГО** | **$0** |

---

## 🆘 ЕСЛИ НЕ РАБОТАЕТ

### Ошибка: Invalid Groq API Key
```
✅ Решение:
1. Откройте https://console.groq.com/
2. Скопируйте ключ полностью (без пробелов)
3. Вставьте в БЛОК 3
```

### Ошибка: Google Drive not mounted
```
✅ Решение:
1. Откройте БЛОК 4
2. Нажмите ▶️
3. Разрешите доступ (нажмите "Разрешить")
```

### Ошибка: No photos found
```
✅ Решение:
1. Создайте папку на Drive: Menu_Parser/photos
2. Загрузите фото в эту папку
3. Нажмите ▶️ БЛОК 11
```

### Низкое качество OCR
```
✅ Решение:
1. Используйте четкие фото (1080+ px)
2. Хороший контраст
3. Нет бликов и теней
```

---

## 📊 ОЖИДАЕМЫЙ РЕЗУЛЬТАТ

### На входе (фото меню):
```
[Фото с текстом: "Капучино - 180р"]
```

### На выходе (CSV):
```
70000001048209528|Капучино|180
```

### На выходе (XML):
```xml
<item>
  <n>Капучино</n>
  <price>180</price>
</item>
```

---

## 🎯 СТАТУС ПРОЕКТА

| Что | Статус |
|-----|--------|
| OCR (Tesseract) | ✅ Работает |
| LLM (Groq) | ✅ Бесплатно |
| Google Drive | ✅ Интегрирован |
| CSV экспорт | ✅ Готов |
| XML экспорт | ✅ Готов |
| Русский язык | ✅ Поддерживается |
| Notebook (.ipynb) | ✅ Готов |

---

## 🔄 WORKFLOW

```
Фото меню
    ↓ (Tesseract OCR - БЕСПЛАТНО)
Распознанный текст (с опечатками)
    ↓ (Groq LLM - БЕСПЛАТНО)
Структурированные данные
    ↓ (Форматирование)
CSV + XML файлы
    ↓ (Google Drive)
Готовые результаты ✅
```

---

## 📱 МОБИЛЬНАЯ ВЕРСИЯ

Если работаете с телефона:

```
1. Откройте Google Colab в браузере
2. Загрузите notebook
3. Точки трёх линий → Mobile
4. Запускайте как обычно
```

---

## 🎓 ПРИМЕРЫ ID РЕСТОРАНОВ

Как найти ID 2ГИС:

```
Откройте ресторан на 2ГИС:
https://2gis.ru/vladivostok/firm/70000001048209528
                                    ↑
                            Это и есть ID!
```

---

## 📞 ПОДДЕРЖКА

### Groq не работает?
→ https://console.groq.com/ (проверить статус)

### Google не работает?
→ https://www.google.com/appsstatus (проверить статус сервисов)

### Colab не работает?
→ https://colab.research.google.com/ (попробовать заново)

---

## ✨ ГОТОВО!

**Вы установили полностью бесплатный парсер меню!** 🎉

Запускайте и получайте результаты в Google Drive!

**Стоимость: $0** ✅

---

## 📚 ПОЛНАЯ ДОКУМЕНТАЦИЯ

Если нужны подробности:

1. **Быстрый старт**: БЕСПЛАТНАЯ_ВЕРСИЯ_README.md
2. **Получить ключ**: ПОЛУЧИТЬ_GROQ_КЛЮЧ.md
3. **Код**: menu_parser_free.ipynb (с комментариями)

---

## 🚀 ДАВАЙТЕ НАЧНЁМ!

```
1. Откройте: https://console.groq.com/
2. Нажмите: Create API Key
3. Скопируйте ключ
4. Откройте: https://colab.research.google.com/
5. Загрузите: menu_parser_free.ipynb
6. Вставьте ключ в БЛОК 3
7. Нажмите: ▶️ БЛОК 11

ГОТОВО! ✅
```

**Времени потребуется: 5-10 минут**
**Денег потребуется: $0**
