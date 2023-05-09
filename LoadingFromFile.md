start


### [`.txt и .csv`](#формат-txt-и-csv)

- [x] описание 1

картинка окна

- [x] описание 2
```js
&НаКлиенте
Процедура ПутьКФайлуНачалоВыбора(Элемент, ДанныеВыбора, ВыборДобавлением, СтандартнаяОбработка)
	
	Проводник = Новый ДиалогВыбораФайла(РежимДиалогаВыбораФайла.Открытие);
	Проводник.Заголовок = "Проводник";
	Проводник.Каталог = "P:\Table\обучение программированию";
	
	Если Объект.Формат = "TXT" Тогда 
	  	Фильтр = "Текстовый документ (*.txt)|*.txt";
		
	ИначеЕсли Объект.Формат = "CSV" Тогда 
	  	Фильтр = "Текстовый документ (*.csv)|*.csv"; 
		
	ИначеЕсли Объект.Формат = "XLSX" Тогда 
	  	Фильтр = "Файл Excel (*.xlsx)|*.xlsx";
		
	ИначеЕсли Объект.Формат = "DBF" Тогда 
	  	Фильтр = "Таблица DBF (*.dbf)|*.dbf";
		
	ИначеЕсли Объект.Формат = "XML" Тогда 
	  	Фильтр = "XML-файл (*.xml)|*.xml";
		
	ИначеЕсли Объект.Формат = "JSON" Тогда 
	  	Фильтр = "JSON-файл (*.json)|*.json";	
		
	Иначе 
		Возврат;
		
	КонецЕсли;
		
	Проводник.Фильтр = Фильтр;
	
	Оповещение = Новый ОписаниеОповещения("ПослеВыбораФайла", ЭтотОбъект);
	
	Проводник.Показать(Оповещение);
	
КонецПроцедуры
```

`содержание процедуры «ПослеВыбораФайла»`

```js
Процедура ПослеВыбораФайла (ВыбранныеФайлы, ДополнительныеПараметры) Экспорт
		
	Если ВыбранныеФайлы = Неопределено Тогда 
		Возврат;	
	КонецЕсли;
	
	Объект.ПутьКФайлу = ВыбранныеФайлы [0];

КонецПроцедуры
```

[1]: - [x] описание команды прочитать
```js
&НаКлиенте
 Процедура Прочитать(Команда)
	
	Объект.СоставДокумента.Очистить();
	
	Если Объект.Формат = "TXT" ИЛИ Объект.Формат = "CSV" Тогда 
		
		ПрочитатьФайлTXTилиCSV();
		
	ИначеЕсли Объект.Формат = "XLSX" Тогда 
		
		ПрочитатьФайлXLSX();
		
	ИначеЕсли Объект.Формат = "DBF" Тогда 
		
		ПрочитатьФайлDBF();
		
	ИначеЕсли Объект.Формат = "XML" Тогда 
		
		ПрочитатьФайлXML();	
		
	ИначеЕсли Объект.Формат = "JSON" Тогда 
		
		ПрочитатьФайлJSON();
		
	КонецЕсли;
		
КонецПроцедуры
```

### `формат txt и csv`
sdgf
sg
fgf
gsf
g
sg
s
sgfgs