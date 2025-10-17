# Документация параметров конфигурации объекта поиска

## Таблица параметров

| Параметр | Тип | Описание | Пример значения |
|----------|-----|----------|-----------------|
| **Основные параметры** |
| `seasonPassIDConfig` | `string` | Идентификатор конфигурации сезонного пропуска | `""` |
| `objectParamID` | `string` | Уникальный идентификатор параметра объекта | `"RLF_Lootable_Hay"` |
| `buildingTypeParamIDHandle` | `object` | Обработчик параметров типа здания, для конкретного здания и типа лута | `{}` |
| **Текстовые параметры** |
| `objectTitle` | `string` | Заголовок/название объекта (ключ локализации) | `"#STR_OS_Hay"` |
| `objectCustomIcon` | `string` | Путь к пользовательской иконке объекта | `""` |
| `actionText` | `string` | Текст действия при взаимодействии (ключ локализации) | `"#STR_OS_SearchAction #STR_OS_Small_Hay"` |
| `emptyText` | `string` | Текст, отображаемый когда объект пуст | `""` |
| **Аудио параметры** |
| `registeredSoundSet` | `string` | Идентификатор набора звуков для воспроизведения | `"RLF_garbagesearching_SoundSet"` |
| **Параметры времени** |
| `coolDownAfterSearchInMin` | `number` | Время кулдауна после поиска (минуты) | `0` |
| `timeToSearch` | `number` | Время выполнения поиска (секунды) | `3.0` |
| **Параметры урона** |
| `chanceToDamageHands` | `number` | Шанс получить порез рукам (0.0 - 1.0) | `0.0` |
| `damageToGloves` | `array[number]` | Урон для перчаток по уровням fact, если 1 параметр -1 то min, max| `[0.0, 0.0, 0.0]` |
| `damageHandsFindedItemClassContains` | `array[string]` | Классы предметов, наносящие урон рукам при находке | `[]` |
| **Ограничения поиска** |
| `searchOnlyEmptyHands` | `number` | Поиск только с пустыми руками (0=нет, 1=да) | `0` |
| `enableIsKindOfItemInHands` | `number` | Включить проверку родителя предмета в руках (0=нет, 1=да) | `0` |
| `ignoredObjectsInHands` | `array[string]` | Список игнорируемых объектов в руках | `[]` |
| **Списки объектов** |
| `objectsList` | `array[string]` | Список классов объектов для поиска | `["farm_strawstack", "misc_haybale"]` |
| `ignoredObjectsList` | `array[string]` | Список игнорируемых объектов | `[]` |
| `uiWindowShowOffset` | `map[string, vecotr]` | Список объектов для которых необходимо переопределить центр объекта (если плашка где то не там находится вы можете ее поднять или опустить) | `[]` |
| **Параметры инструментов** |
| `enableIsKindOfForTool` | `number` | Включить проверку родителя инструмента (0=нет, 1=да) | `0` |
| `findWithToolMode` | `number` | Режим поиска с инструментом. Если 1 то необходимо искать с инструментом. Если 0 то сначала открыть инструментом, потом искать. | `1` |
| `toolsToOpenList` | `array[string]` | Список инструментов для открытия/поиска | `["Pitchfork"]` |
| `addHealthToToolAfterUse` | `array[number]` | Изменение прочности инструмента fact, если 1 параметр 0 то min, max| `[0.0, 0.0, 0.0]` |
| `addQuantityToToolAfterUse` | `array[number]` | Изменение количества инструмента fact, если 1 параметр 0 то min, max| `[0.0, 0.0, 0.0]` |
| **Зоны** |
| `blockZones` | `array` | Список заблокированных зон | `[]` |
| `blockZonesRadius` | `array` | Радиусы заблокированных зон | `[]` |
| `tierZonesList` | `array` | Список зон по уровням | `[]` |

```json
{
        "seasonPassIDConfig": "",
        "objectParamID": "RLF_Lootable_PostBox",
        "buildingTypeParamIDHandle": {},
        "objectTitle": "#STR_OS_PostBox",
        "objectCustomIcon": "relife_ObjectSearch/images/objects_icons/postal-box.edds",
        "actionText": "#STR_OS_SearchAction #STR_OS_Small_PostBox",
        "emptyText": "",
        "registeredSoundSet": "RLF_knigi_looting_SoundSet",
        "coolDownAfterSearchInMin": 0,
        "timeToSearch": 3.0,
        "chanceToDamageHands": 0.0,
        "damageToGloves": [
            0.0,
            4.0,
            8.0
        ],
        "damageHandsFindedItemClassContains": [],
        "searchOnlyEmptyHands": 0,
        "enableIsKindOfItemInHands": 0,
        "ignoredObjectsInHands": [],
        "showMiniGame": 0,
        "miniGameType": 0,
        "miniGameSettings": {
            "lp_RequiredHits": 0,
            "lp_RotationSpeed": 0.0,
            "lp_RandomRotation": 0,
            "lp_TimeToOpen": 0.0,
            "lp_TimePenalty": 0.0,
            "lp_TimeBonus": 0.0,
            "lp_TargetTolerance": 0.0,
            "sg_TotalCount": 0
        },
        "miniGameToolsNeed": [],
        "objectsList": [
            "RLF_Lootable_PostBox",
            "postbox1",
            "postbox2"
        ],
        "ignoredObjectsList": [],
        "uiWindowShowOffset": {
            "misc_postbox1.p3d": [
                1.0,
                -0.4000000059604645,
                0.0
            ]
        },
        "selectionNeed": {},
        "enableIsKindOfForTool": 0,
        "disableRegisteredSoundSet": 0,
        "toolActionAnimHandler": {},
        "findWithToolMode": 0,
        "toolsToOpenList": [],
        "addHealthToToolAfterUse": [
            0.0,
            4.0,
            8.0
        ],
        "addQuantityToToolAfterUse": [
            0.0,
            4.0,
            8.0
        ],
        "blockZones": [],
        "blockZonesRadius": [],
        "tierZonesList": [
            {
                "tierName": "Tier1",
                "objectParamID": "CustomParamID",
                "buildingTypeParamIDHandle": {
                    "HouseType": "paramID"
                },
                "zonesList": [
                    [
                        0.0,
                        0.0,
                        0.0
                    ]
                ],
                "zonesRadiusList": [
                    0
                ]
            }
        ]
    },
```
