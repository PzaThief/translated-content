---
title: keyTimes
slug: Web/SVG/Attribute/keyTimes
translation_of: Web/SVG/Attribute/keyTimes
---
« [SVG Attribute reference home](/ru/docs/Web/SVG/Attribute "en-US/docs/Web/SVG/Attribute")

Атрибут `keyTimes` представляет собой разделённый точками с запятой список значений времени, используемых для управления темпами анимации. Каждое значение в списке соответствует значению в списке атрибутов {{ SVGAttr("values") }} и определяет, когда оно используется в анимации. Каждое значение времени в списке `keyTimes` задаётся как значение с плавающей запятой от 0 до 1 (включительно), представляющее пропорциональную величину смещения в течение элемента анимации.

Если указан список `keyTimes`, то в списке `keyTimes` должно быть ровно столько же значений, сколько в списке {{ SVGAttr("values") }} .

Каждое последовательное значение времени должно быть больше или равно предыдущему значению времени.

Семантика списка keyTimes зависит от режима интерполяции:

- Для линейной и сплайновой анимации первое значение времени в списке должно быть равно 0, а Последнее значение времени в списке должно быть 1. Ключевое время, связанное с каждым значением, определяет, когда значение задаётся; значения являются интерполяцией между ключевыми моментами.
- Для дискретной анимации первое значение времени в списке должно быть равно 0. Время, связанное с каждым значением, определяет, когда значение задаётся; Функция анимации использует это значение до следующего времени, определённого в `keyTimes`.

Если в качестве режима интерполяции используется _paced_, атрибут `keyTimes `игнорируется.

Если в качестве параметра длительности выбрано _indefinite_, атрибут `keyTimes` игнорируется.

## Usage context

| Categories         | Animation value attribute                                                        |
| ------------------ | -------------------------------------------------------------------------------- |
| Value              | \<list>                                                                          |
| Animatable         | No                                                                               |
| Normative document | [SVG 1.1 (2nd Edition)](http://www.w3.org/TR/SVG/animate.html#KeyTimesAttribute) |

## Пример

```html
<?xml version="1.0"?>
<svg width="120" height="120"
     viewPort="0 0 120 120" version="1.1"
     xmlns="http://www.w3.org/2000/svg">

    <circle cx="60" cy="10" r="10">

        <animate attributeName="cx"
                 attributeType="XML"
                 dur="4s"
                 values="60 ; 110 ; 60 ; 10 ; 60"
                 keyTimes="0 ; 0.25 ; 0.5 ; 0.75 ; 1"
                 repeatCount="indefinite"/>

        <animate attributeName="cy"
                 attributeType="XML"
                 dur="4s"
                 values="10 ; 60 ; 110 ; 60 ; 10 "
                 keyTimes="0 ; 0.25 ; 0.5 ; 0.75 ; 1"
                 repeatCount="indefinite"/>

    </circle>
</svg>
```

**Демонстрация**

{{ EmbedLiveSample('Пример','120','120') }}

## Элементы

Следующие элементы могут использовать атрибут `keyTimes`

- {{ SVGElement("animate") }}
- {{ SVGElement("animateColor") }}
- {{ SVGElement("animateMotion") }}
- {{ SVGElement("animateTransform") }}