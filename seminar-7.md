## Корпусные приложения: N-gram Viewer, SketchEngine, AntConc

### N-gram Viewer

[Google Ngrams](https://books.google.com/ngrams) – поисковый онлайн-сервис компании Google, позволяющий строить графики частотности языковых единиц на основе огромного количества печатных источников, опубликованных с 16 века и собранных в Google Books. Аналогичные возможности на русском языке предоставляет также [НКРЯ](http://ruscorpora.ru/search-main.html), где имеется сервис «Графики».

**N-грамма** — последовательность из _n_ слов. Последовательность из двух последовательных элементов часто называют _биграмма_, последовательность из трёх элементов называется _триграмма_. Не менее четырёх и выше элементов обозначаются как_ N-грамма_, N заменяется на количество последовательных элементов.

Использование данных при поиске и построении графиков ограничено N-граммами: для построения графика N-грамма должна встречаться в соответствующем корпусе не менее 40 раз.

Частотность – процент искомой единицы от числа соответствующих единиц \(слово относительно всех слов, биграммы относительно всех биграмм и т.д.\).

##### О кнопках:

**case-insensitive** – при установке флажка в окне система не различает заглавные и строчные буквы;

**between ... and ...** – между ... и... \(окно указания временного периода, вводится год начала исследования и конца исследования\);

**from the corpus** – из корпуса \(выбрать из выпадающего меню\);

![](https://lh5.googleusercontent.com/B06ONokWApeu-6bIbUx73WryIxGsdQz0-hZx-30K-bXHkP2EpGQL6I9YPQ8A7R3yfZuKFBCo9fJ90VaVl3cg-Vbrun5NlUs_-m4yrA0ODLkpxqXxbBLv7CGMNmsFLEpo79K25LK0wc2AADT0xQ)

**with smoothing** – со сглаживанием \(выбрать из выпадающего меню\);

**search lots of books** – искать в массивах книг \(кнопка команды на поиск и построение графика\).

Кроме построения графиков, система представляет ссылки к текстам, найденным по запросам. Как правило, это библиографические описания книг и фрагменты текстов с выделением в них цветом заданных N-грамм. В некоторых случаях доступен полный текст книги в графическом формате.

##### Запросы

Чтобы получить сравнить частотности нескольких единиц, запишите их через запятую.

![](/assets/Снимок экрана 2018-03-16 в 1.32.14.png)

По умолчанию поиск осуществляется с учетом регистра: если вы хотите это изменить, поставьте соответствующий флажок.

По умолчанию осуществляется поиск конкретных словоформ \(как _Точный поиск_ в НКРЯ\), если вы хотите искать все словоформы, припишите \_INF в конце слова \(например: птица\_INF\)

![](/assets/Снимок экрана 2018-03-16 в 1.24.26.png)

Если вместо одного из слов поставить астериск, то буду показаны 10 самых частотных биграмм со вторым словом:

![](/assets/Снимок экрана 2018-03-16 в 1.26.53.png)

Искать можно не только конкретные слова, но их грамматические характеристики.

![](/assets/Снимок экрана 2018-03-16 в 1.28.58.png)

![](https://lh4.googleusercontent.com/0diI5K1jJbVH8jdloY52FldZp3KHF26zQ9QumAsg7NCh6QxQqbe2JTnFcJcXVoLujYn0mV7pXK9IAOpJkl8pmdHCvv1Mznrn6yKDF3cDU6W1YRLRI1mpPuFNeCWKhyAacPfjkAGSlKkoJpt0QQ)

##### Cравнение Google NGrams и НКРЯ \(данные за 2012 год\)

| Характеристика | НКРЯ | Google books \(rus\_2012\) |
| :--- | :--- | :--- |
| Объем корпуса \(число документов\) | 85 996 | 591 310 |
| Число словоупотреблений | 229 968 798 | 67 137 666 353 |
| Единицы частоты употребления      N-грамм | IPM \(Instances per million – число употреблений N-граммы на миллион словоупотреблений\) | Проценты \(число употреблений N-граммы на сто употреблений последовательностей той же длины\) |
| Система письма | Большинство текстов основного корпуса частично представлены в современной системе письма, но некоторая часть текстов – в старой орфографии | Тексты представлены как в современной , так и в старой системе письма. Однако при поиске текстов в старой системе письма имеются проблемы |
| Операции над графиками | невозможны | возможны |
| Возможности отбора материала | создание пользовательских подкорпусов по разным критериям | Отбор материала и построение графиков осуществляется только по году издания. |

##### Операции над графиками

**Суммирование \(сложение\) графиков.** \(стол+стола+столов\)

Операция позволяет суммировать значения каждой точки двух или более графиков. Для осуществления операции поисковые слова вводятся в окно через знак +, например: лошадь + лошади +лошадей.

**Вычитание графиков.** \(перст-палец\)

Операция позволяет вычитать из значения каждой точки графика, значение той же по горизонтали точки другого графика. С помощью этой операции можно представить, насколько частота встречаемости одной N-граммы больше \(меньше\) другой, и как это различие менялось во времени. Для осуществления операции поисковые слова вводятся в окно через знак «-», например, _вежливость-корректность_. Все выражение следует взять в круглые скобки: \(вежливость-корректность\). При этой операции вся кривая или её часть может находиться в области отрицательных значений.

**Умножение графиков.** \(марксизм\*100\), марксизм

Операция позволяет умножать на _n_ значения всех точек графика. Операция умножения позволяет сделать сопоставимым поведение кривых, значения которых отличаются на несколько порядков. Слова в поисковое окно вводятся следующим образом: слово знак «\*» множитель, например, лемматизация\*100.

**Деление графиков.** \(сапоги/валенки\),сапоги,валенки

Делить значение каждой точки графика на значение точки другого графика, имеющий ту же координату горизонтальной оси. Операция позволяет установить, во сколько раз один термин встречается чаще другого.Слова в поисковое окно вводятся следующим образом: слово – делимое, знак «/», слово – делитель, например сапоги/валенки.

Примечание. Операцию деления нельзя использовать по тому же типу, что операцию умножения. Выражение Время/100 означает, что система покажет, во сколько раз в текстах БД слово «время» встречается чаще \(реже\) чем цифра 100, а не уменьшит результат в сто раз. Это делает невозможной операцию вычисления средней встречаемости нескольких терминов.

### SketchEngine

[SketchEngine](https://the.sketchengine.co.uk/)

_Sketch Engine_ – система, позволяющая изучать сочетаемость слов на основе корпусов разных языков, причем не просто по соседству в тексте, а по грамматическим отношениям.

![](https://lh4.googleusercontent.com/p-VK8YogigRphmp50l_Wf1EQ8ThqG-1lj0pUkPbiUn_eEq6tRuxWPMODggsE0HPA83FqFvnUji-ot1eK-CWH5nQZZS7iNW_VzOTsIRH0gQ6_XCseYJTtjoPz0DV_-W1OvqB4lvsX)

![](https://lh6.googleusercontent.com/DV_lyaSvjSsXJ2iIypqAoNdvSXp_3BUYgaLq_0AtkecyFlBNOV32VdCwY9qw0EPr1Pjsm7aspMotUGaVUJ9xKf_XH9WA7sUYjZJdSvI-0oTQ2fA7Q_AaKpWJKklT3e9cYFx8fxoK)

![](https://lh4.googleusercontent.com/oROllQJRX_0FMfS8EuK8PmIV0P7Q8o226usTndb1s9G3XDRMz1sLS-G-JPNmt_sBFT-r8H7pIb-FfsTY-rVcK366uavKuU19ov97vZDVxxQzjQu6sz3fUf_eImpdpOG2lpIwGdfA)

### AntConc

[Download AntConc](http://www.laurenceanthony.net/software/antconc/)

С помощью данной программы можно производить поиск и подсчет различных элементов текста, анализировать частотность и контекст употребления словоформ, словосочетаний и морфем, сравнивать употребительность словоформ в разных текстах.

Отсутствие морфологического анализатора частично компенсируется возможностью подключения пользовательского списка лемм. Программа может быть использована для получения привязанных к заданной предметной области словарных минимумов, списков устойчивых сочетаний \(в том числе терминологических\), выборок к тематическим группам слов.

Проще говоря, это программа, которая позволяет создать собственный корпус. Чтобы загрузить файл в меню _File_ нажимаем «Open File» \(файл должен быть в формате .txt/.xml/.html\).

1.Открываем во второй сверху строке меню кнопку «Word List» \(вторяя слева\) и нажимаем кнопку «Start» \(внизу ближе к левому краю\). Программа выстроит все словоформы текста в порядке частотности

2.Можно сортировать и по другим критериям. Если вместо «Sort by Freq» \(в самом низу\) выбрать «Sort by Word», произойдет сортировка по алфавиту, если выбрать «Sort by Word End», сортировка пойдет по концу слов.

3.Если к тому же поставим галочку между фразами «Sort by» и «Invert Order», то сортировка пойдет в обратном порядке — от редких слов к частым или от _я_ до _а_.

4.Можно кликнуть из списка любое слово, начнется его автоматический поиск в окне _Concordance_.

**Конкорданс **– это список всех употреблений заданного языкового выражения \(например, слова\) в контексте, возможно, со ссылками на источник.

\(В НКРЯ нечто похожее было тогда, когда мы выводили в KWIC.\)

Если открыто окно _Concordance_, искомое слово можно ввести в окошко, находящееся между кнопкой «Start» и фразой «Search Term» и нажать «Start». Будет происходить поиск данного слова в контекстах.

![](/assets/Снимок экрана 2018-03-16 в 10.46.28.png)

Если убрать галочку над тем же окошком между словами «Search Term» и «Words», можно будет искать не только конкретную форму слова, но и похожие формы: например, пишем пункт — выйдет пункта, пункты и т. п.

Кроме того можно использовать следующие специальные символы:

![](/assets/lkjhgimport.png)

![](/assets/Снимок экрана 2018-03-16 в 10.50.27.png)

![](/assets/Снимок экрана 2018-03-16 в 11.05.43.png)

Вы можете сохранить результаты вашего поиска в отдельный файл: во вкладке _File_ –&gt; «Save Output».

**График конкорданса \(Concordance Plot\). **В этом инструменте все адреса для каждого элемента поиска представлены в виде «штрих-кода», указывающего на место в файле, где находится элемент. График позволяет увидеть, какие файлы включают искомый элемент. Он также может быть использован для определения места, где сталкиваются искомый элемент и кластер. Во вкладке _File View_ вы можете посмотреть расширенный контекст, в котором встречается искомое слово.

![](/assets/Снимок экрана 2018-03-16 в 10.52.32.png)

**Кластеры \(Clusters\). **Инструмент _кластеры_ используется для создания упорядоченного списка кластеров, которые появляются вокруг поиска в целевом файле, перечисленные в левой части главного окна. С помощью функции _Cluster Size_ мы можем изменять длину искомой последовательности. _Search Term Position_ задаёт позицию искомого слова внутри N-граммы.

![](/assets/Снимок экрана 2018-03-16 в 10.58.52.png)

**Коллокации \(Collocates\)**. Кластеры показывают N-граммы, которые встречаются в тексте \(т.е. слова, которые стоят рядом друг с другом непосредственно\), тогда как в списке коллокаций мы видим слова, которые статистически часто встречаются с искомым словом \(слова, находящиеся в «окне поиска» – _Window Span_\).

Freq\(R\) насколько часто встречается данное слово справа от искомого

Freq\(L\) насколько часто встречается данное слово слева от искомого

Freq насколько часто встречается данное слово вместе с искомым

Stat вероятность того, что данные слова встретятся вместе относительно того насколько часто они встречаются по отдельности.

![](/assets/Снимок экрана 2018-03-16 в 10.59.14.png)

**Список слов. **Данный инструмент подсчитывает все слова в корпусе и представляет их в упорядоченном списке. Это позволяет быстро найти, какие слова употребляются наиболее часто в корпусе.

**Список ключевых слов. **В дополнение к созданию списка слов, с помощью _AntConc_ можно сравнить слова в целевом файле со словами, которые появляются в «базисном корпусе», чтобы создать список "Ключевых слов", которые являются наиболее частыми \(или редкими\) в целевых файлах.

### Полезные ссылки

[NGram Viewer User Guide](http://gf.nsu.ru/www/wp-content/uploads/2015/11/Google-Books-NGram-Viewer.pdf)

[Sketch Engine User Guide](https://www.sketchengine.co.uk/user-guide/user-manual/)

[Advanced Usage of Google NGram Viewer](https://books.google.com/ngrams/info#)

[AntConc User Guide](http://www.laurenceanthony.net/software/antconc/resources/help_AntConc321_english.pdf)

[AntConc Help](http://www.laurenceanthony.net/software/antconc/releases/AntConc352/help.pdf)

[AntConc handout](https://hfroehlich.files.wordpress.com/2014/05/corpus-linguistics-with-antconc-hgf-handout.pdf)

[Corpus Analysis with AntConc](https://programminghistorian.org/lessons/corpus-analysis-with-antconc)[ ](https://programminghistorian.org/lessons/corpus-analysis-with-antconc)\(tutorial\)

[Sample Corpus](https://www.dropbox.com/s/cmt0m8wxcj78hh8/sample_corpus.txt?dl=0)

 

