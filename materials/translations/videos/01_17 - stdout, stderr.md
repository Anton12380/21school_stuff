Welcome to the bonus part of the day. This part isn't mandatory for today's exercises. But it'll be useful for your career as a developer. And for the rest of the bootcamp too. So earlier we talked about standard output Actually, it isn't 100% accurate... There are two types of outputs : standard output, and standard error. So using our favorite example : "cat file.txt" Everything went fine, the file's content is displayed on the standard output. However, if try doing "cat" on a file that doesn't exist, it'll display a message on the error output. Let's say I do a "cat file.txt | rev" The file's being displayed in reverse. Which means the file's content has been displayed on the standard output. The pipe's interpreted the standard output as the "rev"'s standard input and the "rev" has done its job. However, if I do this on a file that doesn't exist... cat will display the error on the standard error channel, "rev" won't read from this error channel, as it only reads from the standard output, which is now its standard input, so the message won't be displayed. It can be interesting. Or not. You may also reverse the error message if you want. How? By adding more redirections, If we want to redirect the standard error channel's message, and handle it as if it was a standard output, we'll do this... So 2 represents the standard error's output. the 1 represents the standard output. We tell it that everything there is on the standard error channel has to be treated as if it was a standard output. So, if we add " | rev ", we can see the message is in reverse. Because it's been treated like a standard output. Identically, we can redirect everything that's in the standard error channel (2) into a file. For example, if I do this ... I'm asking 2 to be redirected into "error" and keep everything that's in "error". we can see our earlier error message And once again, if we do this 2-3 times in a row, it's only displayed once, because it's been overwritten and there's a double redirection, which will allow you to place your error messages at the end of the file. All of this can be quite practical if you have a list of files containing error messages, but you want to keep only the part that worked or only the part that didn't work, etc... Thanks to those redirections, you'll be able to gather all erroneous files into one error file. Something else, that may be useful... a very special file ... that isn't really a file, but oh well... It's called "/dev/null" What is it? Basically, everything that's written towards "/dev/null" will simply be erased. Forgotten. So here, nothing's gonna happen. The "/dev/null" file doesn't really exist. So nothing's been added to it. Whatever. So what can we use it for? We can use it to delete a part, and keep only error messages, for example. If we want to display all error messages, it's a real mess. You need to go back up, check, and stuff... If we tell it "everything worked, redirect this towards /dev/null" ... and there you go! Displaying only error messages. So once again, this may be very practical for debugging or check whether your scripts work as they should. That's something very important to know for the future.



> Am ajuns acum la partea bonus a zilei. 

We've now reached the bonus part of the day.

> Aceasta parte nu e obligatorie pentru a face exercitiile zilei, în schimb va va fi foarte utila in viata voastra de programator, si chiar si pentru resl 

This part is not required to do the exercises of the day, instead it will be very useful in your life as a programmer, and even for the resl

> Mai devreme vorbeam de iesirea standard. 

Earlier I was talking about standard output.

> Daca luam exemplul nostru: daca execut "cat" pe fisier, a mers, totul a functionat corect si totul e afisat pe iesirea standard. 

If we take our example: if you execute " cat " on the file, it worked, everything worked properly and everything is displayed on the standard output.

> In schimb daca-i cer sa afiseze ceva ce nu exista, imi va da un mesaj pe iesirea de eroare. Deci... 

Instead if I ask him to post something that doesn't exist, he'll give me a message about the error output. So ...

> Cum putem vedea asta? Daca fac "cat" pe fisierul si fac "pipe" prin "rev", vom vedea ca fisierul e inversat. 

How can we see that? If I do "cat" on the file and do "pipe" through "rev", we will see that the file is reversed.

> Inseamna ca continutul fisierului a fost scris in iesirea standard, si "pipe" a trimis iesirea standard ca intrare standard pe "rev", si "rev" si-a facut treaba.

It means that the content of the file was written in the standard output, and "pipe" sent the standard output as standard input on "rev", and "rev" did its job.

> In schimb daca acum dau un fisier care nu exista, "cat" va afisa eroarea pe iesirea de eroare, si "rev" nu va citi aceasta iesire de eroare, pentru ca citeste doar intrarea/iesirea standard, si nu va inversa linia de eroare. 

Instead if you now give a file that does not exist, " cat "will display the error on the error output, and" rev " will not read this error output, because only read the standard input/output, and will not reverse the error line.

> Aceasta poate sa fie sau nu interesant: puteti sa vreti sa inversati si aceasta iesire de eroare. 

This may or may not be interesting: you may also want to reverse this error output.

> Cum facem asta? 

How do we do this?

> Cu niste redirectari suplimentare. 

With some additional redirects.

> Daca vrem sa redirectam tot ce e pe iesirea de eroare, si sa tratam rezultatul ca si cum ar fi iesirea standard, vom face asta: "2>&1"

Daca vrem sa redirectam tot ce e pe iesirea de eroare, si sa tratam rezultatul ca si cum ar fi iesirea standard, vom face asta: "2>&1"

> Deci "2" va corespunde iesirii de eroare, "1" va corespunda iesirii standard, si asa ii spunem ca tot ce vine pe iesirea de eroare va fi tratat ca si cum ar fi pe iesirea standard. 

So "2" will correspond to the error output, "1" will correspond to the standard output, and so we say that everything that comes on the error output will be treated as if it were the standard output.

> Daca acum facem "| rev", vom vedea ca mesajul a fost inversat cu succes, pentru ca a fost tratat ca si cum ar fi fost o iesire standard.

If we now do "| rev", we will see that the message was successfully reversed, because it was treated as if it were a standard output.

> In mod similar a ceea ce am avut inainte, putem redirecta tot ce e "2", deci iesire de eroare, intr-un fisier.

Similarly to what we had before, we can redirect everything that is "2", so error output, in a file.

> Daca fac asta, cer sa redirectionez "2" in "error", si apoi ma uit sa vad ce e in "error", vedem mesajul de eroare dinainte.

If I do this, I ask to redirect "2" to "error", and then I look to see what is in "error", we see the error message beforehand.

> Si daca-l facem de mai multe ori, il avem o singura data pentru ca a fost suprascris. 

And if we do it several times, we only have it once because it has been overwritten.

> Si avem redirectarea dubla, care va va permite sa adaugati mesajul la sfarsitul fisierului. 

And we have double redirect, which will allow you to add the message at the end of the file.

> Acest lucru poate fi foarte util daca aveti o lista de fisiere, si aveti erori in ele, si vreti sa recuperati doar partea care a mers sau partea care nu a mers, etc. 

This can be very useful if you have a list of files, and you have errors in them, and you want to recover only the part that went or the part that didn't work, etc.

> Cu aceste redirectari veti putea sa aveti de exemplu toate fisierele care au dat erori in fisierul "error".

With these redirects you will be able to have, for example, all the files that gave errors in the "error" file.

> Alt lucru care va va fi foarte util e un fisier special (care nu e chiar un fisier), "/dev/null". 

Another thing that will be very useful is a special file (which is not even a file), "/ dev / null".

> In mare tot ce e scris spre "/dev/null" va fi pur si simplu sters, "uitat". 

By and large everything written to "/ dev / null" will simply be deleted, "forgotten".

> Deci aici nu se va intampla nimic, fisierul "/dev/null" nu exista cu adevarat, deci rezultatul nu va fi adaugat in el. 

So nothing will happen here, the file "/ dev / null" does not really exist, so the result will not be added to it.

> La ce poate folosi? La a sterge o parte din rezultat, pentru a pastra de exemplu doar mesajele de eroare. 

What can it use? When deleting part of the result, to keep for example only error messages.

> Daca vrem sa avem toate mesajele de eroare, acum e cam dezordine, trebuie urcat ca sa le vedem. 

If we want to have all the error messages, now it's a bit messy, we have to go up to see them.

> Daca-i spunem ca tot ce a functionat sa fie trimis spre "/dev/null", nu mai apar decat mesajele de eroare. 

If we tell him that everything that worked has been sent to "/ dev / null", only the error messages appear.

> Inca o data, acest lucru poate fi foarte util pentru face debug, sau pentru a verifica daca scripturile functioneaza corect, e ceva foarte important de stiut in continuare.

Again, this can be very useful for debugging, or to check if the scripts are working properly, something very important to know next.
