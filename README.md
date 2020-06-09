Сниппет для работы с публикациями/презентациями ЦСО.
=============


Загрузка изображений для материалов
-----------
Изображения хранятся в директории /storage/presentations_img/ИМЯ_СТАТЬИ/ , где `ИМЯ_СТАТЬИ` это папка, созданная специально для отдельного матерериала. Если таковой нет, - необходимо создать. Привязка названия к статье/материалу - приветствуется.
### стандарты изображений. 
Изображение должно быть не более 1000 пикселей по ширине. Контейнер - `.jpg` Размер изображения не должен привышать 300 кб.

Редактирование материалов
-----------
[Инфоблок с презентациями](https://csoprocom.com.ua/bitrix/admin/iblock_list_admin.php?IBLOCK_ID=29&type=aspro_scorp_content&lang=ru&find_section_section=0)

Код материала необходимо вставлять во вкладке `Подробно` с включенным параметром `HTML`

![страница редактирования материала](https://github.com/sikorsky0o/cso_snippets/blob/master/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202020-06-09%20%D0%B2%2011.57.17.png)

### Обязательным является заполнение наименования материала.Вкладка `Элемент` В идеале название не должно быть слишком длинным.Так же для указания авторства использем поле `Автор`
Формат авторства - `Фамилия И. О.`
-----------

[Наименование и автор](https://github.com/sikorsky0o/cso_snippets/blob/master/name%26author.png)

Для публикации материалов на сайте необходимо использовать текстовый редактор. Например: [atom](https://atom.io/)

#### Примеры тегов для форматирования текста ####

Для примера приведу сниппет слайда, а далее уже разберем отдельные теги.
```
<section>
	<h2 class="text-center"></h2>
	<div></div>
	<img src="" alt="" class="img-responsive">
</section>
```
Секция
-----------------------------------

По правилу верхним уровем для одного слайда/смыслового блока (тест + изображения) является тег:
``` 
<section>...</section>
```
Внутри "секции" уже находится контент. (заголовки, текст, изображения, списки)
Рассмотрим теги, в которые необходимо обрамлять контент.

Заголовки
-----------------------------------

Заголовки могут быть разных размеров. от h1 до h5 (где 1 - самый крупный).
Для визуального выделения заголовки отцентровываются. Делать это можно с помощью класса "text-center"
```
<h1 class="text-center">Самый крупный заголовок</h1>
<h3 class="text-left">Этот чуть меньше и прижат к левому краю</h3>
```
#### К слову данные классы монжо применять к любому тегу, который обрамляет текст

Текст
-----------------------------------

Весь текст рекомендовано заключать в тег блока `<div></div>`
### Списки
#### Нумерованный список
```
<ol>
	<li>Первый</li>
	<li>Второй</li>
	<li>Третий</li>
	<li>Четвертый</li>
</ol>

```
#### Маркированный список
```
<ul>
	<li>Первый</li>
	<li>Второй</li>
	<li>Третий</li>
	<li>Четвертый</li>
</ul>
```

### Абзацы
Любой абзац выделяем тегом `<p></p>` (он же - параграф)

Стилизация текста
-----------------
Любой текст (даже содержащийся внутри тегов заголовкой, списков и др) можно отдельно стилизовать. 
#### Выделение жирным
```
<strong>rendered as bold text</strong>
```
#### Выделение подчеркнутым
```
<u>This line of text will render as underlined</u>
```
#### Выделение курсивом
```
<em>rendered as italicized text</em>
```


Пример материала, выполненного по стандарту
--------------
```
<!-- Первый слайд -->
<section>
	<div class="row">
		<h3 class="text-center">Центр сертифицированного обучения ООО «Проком»</h3>
		<br><br><br>
		<h1 class="text-center">Анализ ошибок участников национального отборочного тура олимпиады «IT-Universe 2014/2015»</h1>
		<h1 class="text-center text-italic">Конкурс «Управление предприятием в ERP-системе 1С:Предприятие 8». <br>Производственное планирование</h1>
		<br><br><br>
		<h4 class="text-danger">Докладчик: Чернодуб Ирина Вячеславовна <br>ведущий преподаватель 1С:ЦСО "Проком" </h4>
	</div>
</section>
<hr class="custom-hr">
<!-- Второй слайд -->
<section>
	<ol>
		<li>Постановка задачи с учетом пояснений</li>
		<li>Описание исходных данных</li>
		<li>Получение информации в отчетах: неисполненные заказы покупателей и наличие складских остатков для их обеспечения</li>
		<li>Описание ситуаций, требующих принятия управленческих решений. Пояснения к выполнению</li>
		<li>Выводы и рекомендации</li>
        <div></div>
	</ol>
</section>
<hr class="custom-hr">
<!-- Третий слайд -->
<section>
	<h2 class="text-center">Сведения о предприятии ООО «Авангард»</h2>
	<div>
		<p>
			Предприятие ООО «Авангард» занимается <b>производством мебели</b> и <b>оптовой торговлей выпущенной продукции.</b> <br>

			Выпуск готовой продукции на предприятии отражается <b>под заказы на производство,</b> которые должны <b>обеспечить потребности заказов покупателей</b> с учетом дат отгрузки. Вся выпущенная продукция <b>резервируется</b> на складе под клиента. <br>

			При оформлении заказов на производство отслеживается доступный остаток сырья и материалов по складам, необходимый для обеспечения потребностей. Если выявлено, что сырья недостаточно, то <b>оформляются заказы поставщикам.</b><br>

			Для гарантированного обеспечения заказов на производство, используются:
			<ul>
				<li>схемы резервирования сырья и материалов на складах, находящихся в свободном остатке;</li>
				<li>размещения в заказах поставщикам. </li>
			</ul>
		</p>

	</div>
</section>
```
