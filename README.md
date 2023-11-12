## WP SEO and Markup requirements

1. В верстке `h1` тег должен быть только в контентной части страницы, а не в логотипах и в др. местах. Он должен быть только 1 на странице и озаглавливать главный текст страницы.

2. Теги группы `h1` - `h6` нельзя использовать в сайдбарах, футере, хедере. Они должны только разбавлять текст и больше нигде не использоваться. Вместо них использовать нужно `<div>` >, `<span>`, просто стилизованный соответственно.

3. Текстовые блоки нельзя разделять никакими тегами кроме `<p>`, `<strong>` и не добавлять классы, атрибуты. Представьте ситуацию, эти тексты будут в редакторе контента, человек удалил их вместе с атрибутами и классами, и все, верстка сломана. Нужно сделать так, чтобы человек редактируя контент не ломал внешний вид сайта. Если нужно применить стили к текстам - то нужно отталкиваться от вышестоящих оберток.

3.1 <img src="https://i.ibb.co/7zgXC4G/1.png" alt="1" border="0">

4. На списках: `ul`, `ol` - не должно быть тоже классов и атрибутов, так как они вставляются в редакторе и пользователь должен иметь возможность вставить списки и получить нужный внешний вид элементов на странице.

5. На ссылках `<a>` в контенте, в тексте статьи, также не должно быть атрибутов или классов, 

6. Все теги, которые в текстах, редактируемых людьми должны быть без классов и атрибутов.

7. Если есть повторяющиеся по внешнему виду блоки, как на рисунке выше, нужно сделать их модульными, то есть без привязки классами к конкретным страницам. Это нужно для того, чтобы можно было при программировании логики использовать данные блоки в разных частях сайта на разных страницах.

8. При верстке контактных форм также не используем теги `h1` - `h6`, заменяем другими, типа: `<p>`, `<span>`, `<div>` и им подобными.

9. В проекте должен быть 1 файл стилей CSS, и один файл скриптов JS. Стили подключаются в хедере, а скрипты в футере. Это необходимо для улучшения скорости загрузки сайта по Google Page Speed.

10. Если требуется подключить сторонние библиотеки, то их JS должен подключаться в футере в наш основной единый файл, а стили в хедере, также в наш основной файл. Кроме FontsAwesome, их можно отдельно.

11. Не используем Bootstrap, занимаем много места и задерживает загрузку страницы своими CSS, JS.

12. Меню в футере и в хедере также редактируются с админки, если нужно добавить классы на пункты меню - то в этом случае нужно их добавить на `<li>` теги.

13. Текстовые строки, блоки в футере, хедере также редактируются с админки и к ним применяются те же правила, что и к основному контенту. 

14. Если нужно поставить изображение на фон - то нужно его прописать через атрибут `style=””` в теге, а не в файле стилей CSS.

За основу взята сборка <a href="https://github.com/automattic/_s">automattic</a>