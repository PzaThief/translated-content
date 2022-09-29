---
title: Date
slug: Web/HTTP/Headers/Date
tags:
  - HTTP
  - Reference
  - Заголовок
  - Основной заголовок
translation_of: Web/HTTP/Headers/Date
original_slug: Web/HTTP/Заголовки/Date
---
<div>{{HTTPSidebar}}</div>

<p><strong><code>Date</code></strong> основной HTTP заголовок содержащий дату и время, в которое сообщение было создано.</p>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row">Тип заголовка</th>
   <td>{{Glossary("Основной")}}</td>
  </tr>
  <tr>
   <th scope="row">{{Glossary("Запрещённое имя заголовка")}}</th>
   <td>да</td>
  </tr>
 </tbody>
</table>

<h2 id="Синтаксис">Синтаксис</h2>

<pre class="syntaxbox">Date: &lt;day-name&gt;, &lt;day&gt; &lt;month&gt; &lt;year&gt; &lt;hour&gt;:&lt;minute&gt;:&lt;second&gt; GMT
</pre>

<h2 id="Директивы">Директивы</h2>

<dl>
 <dt>&lt;day-name&gt;</dt>
 <dd>Одно из "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", или "Sun" (регистрозависимое значение).</dd>
 <dt>&lt;day&gt;</dt>
 <dd>Номер дня с ведущим нулём, например "04" или "23".</dd>
 <dt>&lt;month&gt;</dt>
 <dd>Один из "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec" (регистрозависимое значение).</dd>
 <dt>&lt;year&gt;</dt>
 <dd>Год из 4-х символов, например "1990" или "2016".</dd>
 <dt>&lt;hour&gt;</dt>
 <dd>Часы с ведущим нулём, например "09" или "23".</dd>
 <dt>&lt;minute&gt;</dt>
 <dd>Минуты с ведущим нулём, например "04" или "59".</dd>
 <dt>&lt;second&gt;</dt>
 <dd>Секунды с ведущим нулём, например "04" или "59".</dd>
 <dt>GMT</dt>
 <dd>
 <p>Время по Гринвичу. HTTP даты всегда представлены в GMT, а не в локальном времени</p>
 </dd>
</dl>

<h2 id="Примеры">Примеры</h2>

<pre>Date: Wed, 21 Oct 2015 07:28:00 GMT
</pre>

<h2 id="Спецификации">Спецификации</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <th scope="col">Спецификация</th>
   <th scope="col">Название</th>
  </tr>
  <tr>
   <td>{{RFC("7231", "Date", "7.1.1.2")}}</td>
   <td>Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content</td>
  </tr>
 </tbody>
</table>

<h2 id="Поддержка_браузерами">Поддержка браузерами</h2>
<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li>{{HTTPHeader("Age")}}</li>
</ul>