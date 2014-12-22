Отличия:

<ol>
<li>`getComputedStyle` не работает в IE8-.</li>
<li>`clientWidth` возвращает число, а `getComputedStyle(...).width` -- в `px`.</li>
<li>`getComputedStyle` не всегда даст ширину, он может вернуть, к примеру, `"auto"` для инлайнового элемента.</li> 
<li>`clientWidth` соответствует внутренней видимой области элемента, *включая `padding`, а CSS-ширина `width`, при стандартном значении [box-sizing](/box-sizing), соответствует зоне *внутри `padding`*.</li>
<li>Если есть полоса прокрутки, то некоторые браузеры включают её ширину в `width`, а некоторые -- нет. 

Свойство `clientWidth`, с другой стороны, полностью кросс-браузерно. Оно всегда обозначает размер *за вычетом прокрутки*, т.е. реально доступный для содержимого.</li>
</ol>