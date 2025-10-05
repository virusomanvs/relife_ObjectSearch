# Конфигурация объекта для поиска

## Структура конфига

```json
[
    {
        "objectParamID": "RLF_Lootable_Locker",
        "objectTitle": "#STR_OS_Locker",
        "objectCustomIcon": "relife_ObjectSearch/images/objects_icons/school-locker.edds",
        "objectsList": [
            "locker_closed_v1",
            "locker_closed_v2",
            "locker_closed_v3",
            "locker_closed_blue_v1",
            "locker_closed_blue_v2",
            "locker_closed_blue_v3",
            "RLF_Lootable_Locker"
        ],
        "ignoredObjectsList": ["open"],
        "enableIsKindOf": 0,
        "toolsToOpenList": [
            "Crowbar",
            "FirefighterAxe",
            "Pickaxe",
            "WoodAxe",
            "RLF_Melee_ApoAxe",
            "RLF_Tools_ConcretePickaxe",
            "SledgeHammer"
        ],
        "damageToGloves": [0, 4, 8],
        "addHealthToToolAfterUse": [0, 4, 8],
        "addQuantityToToolAfterUse": [0, 4, 8],
        "actionText": "#STR_OS_SearchAction #STR_OS_Small_Locker",
        "registeredSoundSet": "RLF_garbagebin_start_SoundSet",
        "emptyText": "",
        "timeToSearch": 3
    }
]
```

## Основные параметры

| Параметр | Тип | Значение | Описание |
|----------|-----|----------|----------|
| **objectParamID** | `String` | `RLF_Lootable_Locker` | Уникальный идентификатор параметров объекта из файла config_ObjectParam.json |
| **objectTitle** | `String` | `#STR_OS_Locker` | Локализованное название объекта (ключ строки) |
| **objectCustomIcon** | `String` | `relife_ObjectSearch/images/...` | Путь к кастомной иконке объекта (формат .edds), можно оставить пустым|
| **timeToSearch** | `Integer` | `3` | Время поиска в секундах |
| **emptyText** | `String` | `""` | Текст при пустом контейнере, если хотите переопределить |

## Списки объектов

### objectsList
Классы объектов или названия p3d, к которым применяются эти параметры:

| Класс | Описание |
|-------|----------|
| `locker_closed_v1` | Закрытый шкафчик, вариант 1 |
| `locker_closed_v2` | Закрытый шкафчик, вариант 2 |
| `locker_closed_v3` | Закрытый шкафчик, вариант 3 |

### ignoredObjectsList
Объекты с этими подстроками в названии будут игнорироваться:

| Значение | Описание |
|----------|----------|
| `open` | Игнорировать объекты со словом "open" (открытые шкафчики) |

## Инструменты для открытия
### enableIsKindOf
| Значение | Описание |
|----------|----------|
| `0` | Отключена проверка наследования классов (точное совпадение) |
| `1` | Включена проверка наследования классов (проверка подклассов) |

### toolsToOpenList
Инструменты, которыми можно открыть объект, если пусто то сразу можно обыскать.

## Параметры износа

Все массивы используют формат `[минимум, базовое значение, максимум]`:

### damageToGloves
Урон перчаткам при поиске, значение без знаков:

| Индекс | Значение | Описание |
|--------|----------|----------|
| `[0]` | `0` | Точное значение |
| `[1]` | `4` | Рандом мин |
| `[2]` | `8` | Рандом макс |

### addHealthToToolAfterUse
Изменение здоровья инструмента после использования, значение без знаков:

| Индекс | Значение | Описание |
|--------|----------|----------|
| `[0]` | `0` | Точное значение |
| `[1]` | `4` | Рандом мин |
| `[2]` | `8` |Рандом макс |

### addQuantityToToolAfterUse
Изменение количества инструмента после использования, значение без знаков:

| Индекс | Значение | Описание |
|--------|----------|----------|
| `[0]` | `0` | Точное значение |
| `[1]` | `4` | Рандом мин|
| `[2]` | `8` | Рандом макс |

## Интерфейс и звук

| Параметр | Значение | Описание |
|----------|----------|----------|
| **actionText** | `#STR_OS_SearchAction #STR_OS_Small_Locker` | Текст действия (локализованный) |
| **registeredSoundSet** | `RLF_garbagebin_start_SoundSet` | Звуковой набор при начале поиска, необходимо зарегистрировать для начала (смотрите инструкцию)|
