# Модели данных

Данное хранилище содержит наработки по моделям данных. Где возможны представлены выдуманные образцы данных.

## Геодезия
1. [Каталог геодезических пунктов](./geodesy/geopoints.xlsx) в формате xlsx позволяет хранить:
- описание геопункта;
- координаты геопункта в различных системах координат.

2. [Метаданные по изысканиям](./geodesy/research-metadata.xlsx) в формате xlsx позволяют хранить:
- общие сведения о съёмке;
- описание, полученных материалов;
- сведения об их хранении;
- описание MosaicDataSet (фишка ArcGis).

3. [Метаданные по изысканиям по ОКС](./geodesy/bldg-metadata.xlsx) в формате xlsx позволяют хранить:
- сведения о материалах, полученных в ходе проектирования, строительства и технического учета построек;
- сведения об их хранении.

## Постройки в ГИС

1. [Классификатор](./bldg/classificat.xlsx) в формате xlsx помогает выделять конструктивные элементы построек.

2. Модель объектов недвижимости для ГИС доступна в формате [plantUml](./bldg/modelER.puml):
![Модель построек](https://www.plantuml.com/plantuml/png/bLN9JXj14BttLxJcaiIIBU0C4ISkaQ98y0CZF2XMl4JsSCaYiMHHOYAKHKg40WJkaHhmaC70-1Ug_oYlgWUxYR0pXiCqLVMgNhrvFInsuh0ThpVgglEirdmUjiE6RhIQhTMdxLOZqd5xFV8orMWjNA_7Iwrc_3X4-idASjIkhTrTiLnx4UdPEI-vKelhqJ0rDwDKp15TAj4UPNHjtr520xjbjydGfTsXQp9sLzjDX3OGx7FARf3HT8Nw7gelAIsLbBgdwH29L2Dy0bX6fqWbEAKSxE5Xw8oXG5xPhaOcuLhxLXgbt50Zdz2PW-7CJGn6xe01VhlesBVR33M2jvyhIgtMmqv71tI0NXy11KVNl0TqIkUkDQz0QQ1UAeqV-a4zEImikBz_EHAeINXlkqbzu2v6XT1dtntsoKZB9D_Io8x9AFb7L7jFYP_uWgDq4frS0zJSW5-Fzf0NuIkEWbD4kg1ZFuceCjnkZTscY1I2qlUN7Zt8MM7ifQoK03DfnsCS1vhwT_D4z8ooVvYI6GtfqO1Iu7Pa3FSnw03XkIBVHoXcq8V7zZMbQF86WGqqD31fAaRJOfLCf0GBZevLM1Bbiij_lGspkoFzwLZMEK5-a3iGb3sXMJ6_MQLIyT3VX2HBO2PZj0VQ0yaJPxoYWm9AHUgBe32r8vHdijpvq9hZiVbRnkqqScdv_IOYbhY7hqTkRFSDWDBCo4n4U6o-mmVc_omEqJkp7r3QWpWI-irsmWxNpiatuPzaRWRAjwkhESkRUbCFS46F9iqx4iY0OJ0eEna1Da4-pUqm_r1NQo6-qbNlM5Mgu4T81xE1RfNBU5OgfM3AEp_ra1aPKX2cb9gAZfv_XHb3EV8dz1nta_mA_xRuSVz2-F7SyuM5larko8wRtNqV_0BVehSJpaLgCMfMyN_xBm00)
[Образец данных](./bldg/sample/) в формате MapInfo.
Обратите внимание, как с помощью символов <> (можно использовать и другие скобки {},[]) иерархическая структура модели  преобразуется в плоскую (например, насосная станция -- часть водозабора, водозабор при этом сам входит в систему водоснабжения):

|Полное наименование|Тип|
|--|--|
|Бугель <дорога>|ДорогаНавес
|Бугель <ниж. посадочная площадка>|Постройка
|Водоснабжение <водозаборный узел на реке Клязьма <насосная станция>>|Постройка
|Водоснабжение <водозаборный узел на реке Клязьма <насосная станция>>|Постройка_Подзем
|Водоснабжение <водозаборный узел на реке Клязьма <насосная станция>>|Вход_люк
|Водоснабжение <водозаборный узел на реке Клязьма <электроснабжение>>|Электр_Низ_0.4кВ
|Водоснабжение <водозаборный узел на реке Клязьма>|Постройка_Подзем
|Водоснабжение <водозаборный узел на реке Клязьма>|Вр
|Водоснабжение <водозаборный узел на реке Клязьма>|КдцВр
|Водоснабжение <водопровод питьевой <камера>>|Камера_Назем
|Водоснабжение <водопровод питьевой <камера>>|Вход_люк
|Водоснабжение <водопровод питьевой>|КдцВп
|Водоснабжение <водопровод питьевой>|Вп
|Водоснабжение <водопровод речной <камера>>|Камера_Назем

