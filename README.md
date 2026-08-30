# Схемы Keysingate

Машиночитаемые схемы документов ядра. Отдаются по адресам, совпадающим с полем
`$id` внутри каждого файла:

| Документ | Адрес |
|---|---|
| `common` | <https://schema.keysingate.com/core/v1/common.json> |
| `emission` | <https://schema.keysingate.com/core/v1/emission.json> |
| `allocation` | <https://schema.keysingate.com/core/v1/allocation.json> |
| `binding` | <https://schema.keysingate.com/core/v1/binding.json> |
| `receipt` | <https://schema.keysingate.com/core/v1/receipt.json> |
| `checkpoint` | <https://schema.keysingate.com/core/v1/checkpoint.json> |
| `closure` | <https://schema.keysingate.com/core/v1/closure.json> |

## Правка

**Этот репозиторий не правится.** Он собирается из источника скриптом
`scripts/publish_schemas.py`; правка здесь будет затёрта следующей сборкой и
до тех пор будет расходиться с реализацией.

## Чего схемы не выражают

Схема ограничивает форму, а не правила. За её пределами остаётся всё, что
требует сравнения нескольких документов или арифметики: покрытие блока
ведомостью, единственность привязки, обязательность `prev_closure` со второго
блока, границы времени, подписи.

**Реализация, проверившая только схему, документ не проверила.**

## Лицензия

Apache License 2.0 — см. `LICENSE`.
