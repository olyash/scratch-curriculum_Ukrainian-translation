Рівень 1

#Фелікс та Герберт

__Передмова:__
Ми збираємось створити гру, в якій __кіт (Фелікс)__ переслідуватиме __мишеня (Герберта)__. Впродовж гри Ви контролюєте Герберта за допомогою мишки, намагаючись втекти від Фелікса.  Що довше Герберту вдається залишатись неспійманим, то більше очок Вам нараховується, тільки не дозволяйте коту впіймати мишеня, бо тоді очки зніматимуться.

##Крок 1: Фелікс рухається за курсором

1. Створіть новий проект. Слідкуйте за своїм просуванням уперед, ставлячи позначки у квадратиках нижче ￼￼￼. 
2. Клікніть на значок Сцена поруч зі списком Спрайтів, перейдіть у вкладці Нове тло (Backdrop) до категорії "У приміщенні"(Indoor) та імпортуйте фон "Зала" (hall). Видаліть оригінальний порожній фон.
2. Переіменуйте спрайт на Фелікс.
3. Переконайтесь, що Фелікс рухається вліво-вправо, натиснувши цю кнопку:
4. Створіть наступний скрипт для Фелікса:

```scratch

	Коли натиснуто зелений прапорець

	завжди

		слідувати за вказіник миші

		переміститись на 10 кроків

		наступний образ

		програти на барабані 62 0.3 удари

	(кінець завжди)
```
		
###Збережіть свій проект

__Натисніть на значок із зеленим прапорцем і перевірте:__
Чи рухається Фелікс за курсором? Чи схожа манера його руху на прогулянку? Чи рухається він з належною швидкістю? 

Збережіть свій проект.

##Крок 2: Фелікс переслідує Герберта

__Нам треба подбати про те, щоб Фелікс переслідував Герберта, а не курсор.__

1. Створіть ще один спрайт за допомогою кнопку вибору спрайтів та оберіть у папці Тварини вкладки Образи спрайт мишеняти.
2. Переіменуйте мишеня на Герберта.
3. Змініть його образ та зробіть його меншим за Фелікса, використовуючи кнопку зменшення спрайту (клікніть 6 разів).
4. Переконайтесь, що Герберт рухається лише вліво-вправо
5. Створіть скрипт, який рухатиме Герберта:

```scratch
	
	Коли натиснуто зелений прапорець
	завжди
		слідувати за вказіник миші
		слідувати за Феліксом
	(кінець завжди)
```

###Збережіть свій проект.
__Натисніть на значок із зеленим прапорцем.__

Чи рухається Герберт разом із мишкою? Чи переслідує Фелікс Герберта?

Збережіть свій проект.

##Крок 3: Фелікс повідомляє про те, що він упіймав Герберта.

__Ми хочемо, щоб Фелікс повідомив нам про те, що  упіймав Герберта.__


1. Змініть скрипт Фелікса на такий:

```scratch
	
	Коли натиснуто зелений прапорець
	завжди
		слідувати за вказіник миші
		переміститись на 10 кроків
		наступний образ
		програти на барабані 62 0.3 удари
		якщо доторкається Герберта
			говорити Спіймав! впродовж 1 сек
		(кінець якщо)
	(кінець завжди)
```

###Збережіть свій проект.

__Натисніть на значок із зеленим прапорцем.__

Чи повідомляє Фелікс про те, що він упіймав Герберта?

Збережіть свій проект.

##Крок 4: Герберт перетворюється на привида після того, як його упіймали. 

__Фелікс не повідомлятиме про те, що спіймав Герберта, натомість Герберт перетворюватиметься на привида, коли його упіймають.__

1. Змініть скрипт Фелікса, щоб він діяв наступним чином, коли кіт спіймає Герберта:

```scratch
	
	Коли натиснуто зелений прапорець
	завжди
		слідувати за вказіник миші
		переміститись на 10 кроків
		наступний образ
		програти на барабані 62 0.3 удари
		якщо доторкається Герберта
			оповістити спіймано
			програти на барабані 58 0.2 удари
		(кінець якщо)
	(кінець завжди)
```
2. Імпортуйте новий образ для Герберта, обравши у вкладці Образи папку Фантазії (Fantasy) і образ "ghost 2-a".
3. Змініть його розмір, натиснувши на кнопку зменшення спрайту (6 разів).
4. Змініть назви образів Герберта таким чином, щоб образ мишеняти називався "живий", а образ привиди "мертвий".
5. Створіть новий скрипт для перетворення Герберта на привида:

```scratch
	
	коли одержую спіймано
	змінити образ на мертвий
	чекати 0.5 сек
	змінити образ на живий
```
	
###Протестуйте свій проект.
__Натисніть на значок із зеленим прапорцем.__

Чи перетворюється Гереберт на привида, коли його спіймано?  
Чи правильні звуки подає Фелікс у відповідний момент? 
Чи дає Фелікс Герберту достатньо часу для втечі?

Збережіть свій проект.

##Крок 5: Набираємо очки


__Введемо функцію накопичування очок, щоб знати наскільки успішно ми зберігаємо життя Герберту. 
Рахунок починатиметься з нуля і збільшуватиметься на 1 за 1 секунду. Коли Фелікс спіймає Герберта, рахунок зменшується на 100.__

1. Створіть змінну для всіх спрайтів під назвою Рахунок. Клікніть на Змінні у вкладці Скрипти і створіть змінну "рахунок".
2. На сцені створіть два наступні скрипти:

```scratch
	
	Коли натиснуто зелений прапорець
	задати значення у 0
	завжди
		змінити значення у 1
		чекати 1 сек
	(кінець завжди)
	
	коли одержую спіймано
	змінити значення у -100
```
	
###Протестуйте свій проект.
__Натисніть на значок із зеленим прапорцем.__

Чи збільшується рахунок на 1 через кожну секунду?  
Чи зменшується рахунок на 100, коли Фелікс ловить Герберта? 
Що відбувається, коли Герберта спіймано ще до того, як гравець набрав 100 очок?  
Чи починається рахунок з нуля, коли стартує нова гра?

Збережіть свій проект.

__Молодець! Проект завершено, тепер можна насолоджуватись грою!__
Не забудьте, що грою можна поділитись з друзями та рідними, натиснувши __"Поділитися цим проектом з іншими"__ у рядку меню.
