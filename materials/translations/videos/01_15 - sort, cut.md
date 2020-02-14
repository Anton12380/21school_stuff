> Now that we've seen how redirections work. We can use this system to keep on handling our files. Let's have a look at a very simple command called "sort". It'll allow you to sort what you're giving it as arguments. So in this case, what you write on the standard input. So here we can see it's sorted all users alphabetically. Be careful, this is a sorting that we call "lexicographic", which means it's based on ASCII's characters sorting, so uppercases are before lowercases. To not have this behavior, you've got options to sort numbers, there are also options to sort in reverse. Do a "man sort", and check out all of its options. Once you've sorted your output, you'll be able to retrieve just the first names, for example. In order to do that, you'll need the "cut" command, which will allow you to cut each line depending on a delimiter. So for example, if I "cut" with the option "-d" on a delimiter, I'll be able to retrieve the fields I've chosen, and if I only want the first fields, I'll just have to add "-f" with "1". As we've seen earlier on, If I add "cat -e" to display non-printable characters I can see that there's a space after "maxime " here. Something I wouldn't have noticed without "cat -e". The "cut" command is very powerful. It'll allow you to do many things. For example, retrieve multiple fields. You may also do a field sort. That should be quite practical to retrieve only information that are important to you. in files like this, that'll be separated by the same delimiter (dot, comma, etc...). Once you've managed to get this result, let's say we keep those first names, we'll be able to modify them. For example, if I want to change "thomas" by "Thomas" I can use the "sed" command, which is a very, very powerful command which allows you to make modifications on data flow. For example you can ask it to turn "thomas" into "Thomas". As we can see here, "Thomas" starts with a capital letter. So what does it do? The first character, the "s" means we're going to "substitute". meaning we're going to replace our 2nd parameter by our 3rd parameter. It's really simple. This is basic "sed" functionalities. However, we can do much more. I'll let you check it out for yourselves. Go have a look at examples on the internet. You can also do "one out of two" modifications. We call those "regex". "regex" are on "patterns", which also are very powerful if you know how to use them. The last file-modification command that we'll see, is called "tr" For example, here we can see the accent in "mélanie". I want to replace it by a normal "e"... "tr" is very simple: it takes 2 arguments, a character and the one we're replacing it with. For example, if we use an "x" to replace the lowercase one in "xavier"... It works. All those commands are pretty basic. Once again, check out their "man". Check out the internet and test them out for yourselves to learn how they work.

Теперь, когда мы увидели, как работают перенаправления, используя эту систему мы сможем продолжить обработку наших файлов. Давайте посмотрим на очень простую команду под названием "sort". Она позволяет сортировать данные вами аргументы, в данном случае, это то, что вы напишите в станд. поток ввода. Итак, тут мы можем увидеть, что были отсортированы имена всех пользователей в алфавитном порядке. Аккуратнее тут, эта сортировка является "лексикографической", что означает, что она основана на сортировке символов согласно ASCII табл., поэтому верхний регистр идет перед нижним регистром. Чтобы изменить работу этой команды, у вас есть опции для сортировки чисел, сортировки в обратном порядке. Введите "man sort", чтобы посмотреть все опции этой команды. После того, как вы отсортировали данные из ст.п.вывода, то через эту команду вы можете получить, к напримеру, только имена. Для этого, вам понадобится команда "cut", которая позволяет вырезать что-либо из каждой строки, в зависимости от разделителя. 
Например, если я выполню "cut" с опцией "-d" (с помощью нее я смогу установить свой разделитель и извлечь выбранные мною поля), я добавлю "-f 1", чтобы извлечь только первые поля в каждой строчке.
Как мы уже с вами видел, если я добавлю "cat -e", чтобы отобразить непечатаемый символы, то я увижу, что тут в строке "maxime " присутствует пробел.
Многие вещи я бы просто не заметил без "cat -e". Команда "cut" имеет очень мощный функционал. С ее помощью вы можете выполнить много разных вещей.
К примеру, извлечь несколько полей. Вы также можете отсортировать эти поля.
Такой подход являться практичным, чтобы извлечь только ту инфомарцию, которая вам важна. Деление полей, в подобных файлах, происходит за счет одного и того же разделителя (точка, запятая и т.д.).
Как только вам удастся получить данный результат, допустим мы продолжим работу с этими именами, мы сможем изменить их. К примеру, если я хочу изменить "thomas" с маленькой буквы на "Thomas" с большой буквы, то я могу воспользоваться командой "sed", которая в свою очередь является мощной, очень мощной командой, которая дает возможность выполнить изменения потока данных. Например, вы можете попросить изменить "thomas" на "Thomas". Как вы тут видите, "Thomas" теперь начинается с большой буквы. Так что же она делает? Первый символ "s" означает "substitute" (заменить), это означает, что мы собираемся заменить 2ой параметр, нашим 3им параметром. Все просто.
Это основы функционала команды "sed".
Однако, мы можем делать гораздо больше. Я даю возможность вам самим все проверить. Идите и посмотрите примеры работы с этой командой в интернете. Вы также можете выполнить "одну из двух" модификаций.
Мы называем все это - "regex" (регулярные выражения). "regex" с использованием "pattern" (строки-образца) также является мощным инструментом, если вы знаете, как ее использовать.
Последняя модификатор-команда, которую мы рассмотрим, называется "tr". К примеру, тут мы можем увидеть знак ударения "mélanie", а я хочу заменить его нормальной "e". "tr" очень проста, она принимает два аргумента, где первый аргумент - символ (который мы хотим заменить), а второй - символ (на который мы меняем).
Например, если мы напишем "X", чтобы заменить маленькую букву в "xavier" ... все получилось. Все эти команды довольно просты. Еще раз, посмотрите их "man". Посмотрите в интернете и протестите их сами, чтобы понять, как они работают.

> Acum ca am vazut cum functioneaza redirectarile, vom putea folosi acest sistem pentru a continua sa manipulam fisierele. 

> Vom vedea о comanda foarte simpla care e "sort". 

> Cum indica si numele, va va permite sa sortati ce ii dati ca parametri, deci ce ii dati sa citeasca de pe intrarea standard in cazul nostru.

> Aici vedem ca a sortat in ordine alfabetica toti utilizatorii.

> Atentie, e о sortare lexicografica, deci bazata pe codul ASCII al caracterelor, deci majusculele sunt inaintea literelor mici.

> Pentru a nu avea acest comportament exista optiuni, alte optiuni pentru a sorta numerele, optiuni pentru a sorta invers. 

> Va las sa cititi "man sort"; ca toate comenzile are multe optiuni. 

> О data sortata iesirea, veti putea de exemplu sa recuperati doar prenumele. 

> Pentru asta exista comanda "cut", care va va permite sa taiati fiecare linie in functie de un delimitator. 

> Keiexemplu daca fac "cut" cu optiunea "jd" pentru delimitator sivoi putea recupera campurile care ma intereseaza. 

> Daca vreau numai primul camp adaug optiunea "-f 1" si recuper doar primele campuri. 

> Revenind la ce am spus mai devreme, adaug optiunea "cat -e" pentru a afisa caracterele non-afisabile, si voi vedea ca aici e un spatiu dupa "maxime", ceea ce nu puteam vedea fara "cat -e". 


> Comanda "cat" e foarte puternica, va permite sa faceti tot felul de lucruri; veti putea de exemplu recupera mai multe campuri, sau о дата de campuri.


> Va fi foarte practic pentru a recupera doar informatiile care va intereseaza  din fisiere de genul acesta care sunt separate prin niste delimitatori, fie prin virgula, fie prin punct si virgula, etc. 


> О data се ati reusit sa vedeti asta, (sa zicem pastrand doar prenumele) vom putea modifies aceste prenume.

> De exemplu daca vreau sa schimb sa zicem "thomas" in "Thomas" (cu majuscula), voi putea folosi comanda "sed". 


> Comanda "sed" e о comanda foarte puternica, ce va permite sa modificati fluxul de date. 


> De exemplu ii vom cere sa schimbe "thomas" in "Thomas". 


> (cu un slash in plus...) 


> Si vedem aici ca "Thomas" incepe acum cu о majuscula. 


> In mare ce face? 


> Primul caractep fs"), spune ca facem о inlocuire, deci vom inlocui al doilea parametru cu cel de-al treilea parametru. 


> E foarte simplu. 


> Е о functionalitate simpla a comenzii "sed", in schimb putem face foarte multe cu aceasta comanda, ьо! deci va sfatuiQSc inca о data sa cititi manualul, sau sa va uitati si la exemple pe Internet, vor fi mai sem initiative.


> Puteti face multe modificari, sa modificati un element din doua, sa folositi expresii regulate, cu diverse modele, lucruri foarte complicate, care pot fi foarte puternice daca reusiti sa le stapaniti bine.


> Ultima comanda de modificare de fisiere pe care о vom vedea se numeste "tr". 


> De exemplu, vedem aici accentul in cuvantul "melanie". 

> Asa il inlocuiesc printr-un "e" normal. 


> tr" e simplu: ia doi parametri, un caracter pe care-l vom inlocui, si un al doilea cu care il vom inlocui. 


> De exemplu pot sa adaug un "X" pentru a schimba "x"-ul din "xavier" in majuscula. 


> Si va face schimbarea. 


> Toate aceste comenzi sunt foarte simple; inca о data: uitati-va la manuale, cautati pe internet, sunt foarte simplu de utilizat, trebuie doar experimentat putin la inceput pentru a vedea cum functioneaza.

Now that we have seen how the redirects work, we will be able to use this system to continue handling the files. We will see the very simple command which is "sort". As the name indicates, it allows you to sort what you give them as parameters, so what you give them to read from the standard entry in our case. Here we see that all users sorted in alphabetical order. Attention, it is a lexicographic sorting, so based on the ASCII code of the characters, so the capital letters are before the small letters. To avoid this behavior there are options, other options to sort the numbers, options to sort the other way around. Once the date has been sorted out, you can for example only recover the first name. For this there is the "cut" command, which will allow you to cut each line according to a delimiter. If I made a "cut" option with the "jd" option for the delimiter saw, I could recover the fields that interest me. If I want only the first field, I add the "-f 1" option and recover only the first fields. Going back to what I said earlier, I add the "cat -e" option to display non-display characters, and I will see that there is a space after "max", which I couldn't see without "cat -e". The "cat" command is very powerful, it allows you to do all kinds of things; for example, you will be able to retrieve more fields, or more fields. It will be very practical to retrieve only the information that interests you from files of this kind that are separated by some delimiters, either by comma or by semicolon, etc. Once you've managed to see this, (let's just keep the first name) we will be able to modify these first names. For example, if I want to change to say "thomas" in "Thomas" (in capital letters), I can use the "sed" command. The sed command is a very powerful command that allows you to change the data flow. For example, we will ask them to change "Thomas" into "Thomas". (with an extra slash ...) And we see here that "Thomas" starts with the capital letter. What's he doing? The first character ("s"), says that we do о replacement, so we will replace the second parameter with the third parameter. It's very simple. It's a command "sed", instead we can do a lot with this command, ьо! so you will advise QSc once you read the manual, or look at examples on the Internet, there will be more initiatives. You can make many changes, modify an element of two, use regular expressions, with different models, very complicated things, which can be very powerful if you manage to master them well. The last file modification command we will see is called "tr". For example, we see here the accent in the word "melanie". That's how I replace it with a normal "e". "tr" is simple: it takes two parameters, one character that we will replace, and a second one that we will replace. For example, I can add an "X" to change the "x" from "xavier" to uppercase. And it will make the change. All these commands are very simple; again: look at textbooks, search the internet, they are very simple to use, you just have to experiment a little at first to see how they work.
