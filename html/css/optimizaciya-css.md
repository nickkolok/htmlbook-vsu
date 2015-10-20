Исходный текст:

```
a:link {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  text-decoration: none;
  font-size: 11px;
  color: #3A681A;
}
a:visited {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #3A681A;
  text-decoration: none;		
}
a:hover {
  text-decoration: none;
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #5CA22E;
}
a:active {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #DC0000;
}
.pole {
  border: 1px solid #008000;
  width: 95px;
  font-size: 11px;
  background-color: #E7F2D7;
  height: 17px;
}
.pole2 {
  border: 1px solid #008000;
  font-size: 11px;
  background-color: #E7F2D7;
  height: 17px;
}
```
1. Группируем `.pole` и `.pole2`
```
a:link {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  text-decoration: none;
  font-size: 11px;
  color: #3A681A;
}
a:visited {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #3A681A;
  text-decoration: none;		
}
a:hover {
  text-decoration: none;
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #5CA22E;
}
a:active {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #DC0000;
}

.pole, .pole2 {
  border: 1px solid #008000;
  font-size: 11px;
  background-color: #E7F2D7;
  height: 17px;
}
.pole {
  width: 95px;
}
.pole2 {
}

```
2. Видим, что от `.pole2` ничего не остаётся. Убираем:
```
a:link {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  text-decoration: none;
  font-size: 11px;
  color: #3A681A;
}
a:visited {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #3A681A;
  text-decoration: none;		
}
a:hover {
  text-decoration: none;
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #5CA22E;
}
a:active {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #DC0000;
}

.pole, .pole2 {
  border: 1px solid #008000;
  font-size: 11px;
  background-color: #E7F2D7;
  height: 17px;
}
.pole {
  width: 95px;
}

```
3. Всякая `a `либо `:link`, либо `:visited`.
Общее этих двух селекторов приписываем просто `a`.
```
a {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  text-decoration: none;		
  font-size: 11px;
  color: #3A681A;
}
a:hover {
  text-decoration: none;
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #5CA22E;
}
a:active {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  font-size: 11px;
  color: #DC0000;
}

.pole, .pole2 {
  border: 1px solid #008000;
  font-size: 11px;
  background-color: #E7F2D7;
  height: 17px;
}
.pole {
  width: 95px;
}

```
4. Наконец, убираем из `a:hover` и `a:active` то, что и так есть в `a`.
```
a {
  font-family: Verdana, Arial, Helvetica, sans-serif;
  text-decoration: none;		
  font-size: 11px;
  color: #3A681A;
}
a:hover {
  color: #5CA22E;
}
a:active {
  color: #DC0000;
}

.pole, .pole2 {
  border: 1px solid #008000;
  font-size: 11px;
  background-color: #E7F2D7;
  height: 17px;
}
.pole {
  width: 95px;
}

```

Ответ получен.
