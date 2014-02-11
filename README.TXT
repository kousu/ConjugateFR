Title: ConjugateFR Readme
Written by: Nick Guenther
Date: July 08 2005
Email: kousue@gmail.com


ConjugateFR is a program to conjugate french verbs. For palm programs, it is
the smallest that I know of and is the only free one available. Also, it is the
only one that has every french tense (even infinitive is included).

Just write in the verb in the field, select the modifiers (elisions, ne..pas),
voice, mood and tense, and tap 'Conjugate' or write a newline.

The algorthm is rule-based (45 rules for regular verbs and 44 for irregulars);
it matches the longest ending it can find (i.e. -ger beats out -er), drops that
ending from the infinitive (in the case of irregulars, this means dropping the
entire word) and adds the proper endings (or the entire word) from the database.
Except for some issues (see KNOWN ISSUES) I believe it to be totally correct,
although by all means test it with obscure verbs and tell me if.

ConjugateFR works on all Palm OSes back to version 2.0. On 1.0 it crashes on
launch. I know the reason for this, but I don't think the effort I'd have to
go to for 1.0 compatibility is worth it.

ConjugateFR was written _ENTIRELY_ with OnBoardC, a free and open source C compiler
for PalmOS, on an Palm m505. Check OnBC out at http://onboardc.sourceforge.net
It was tested on the m505, obviously, and also with a Tungsten and with POSE (how I
know it works with every OS except 1.0).

THERE ARE MANY IRREGULARS AND TINY LITTLE EXCEPTIONS. PLEASE PLEASE PLEASE TELL ME
IF YOU FIND ONE

~*I LOVE EMAIL! PLEASE SUBMIT REVIEWS AND BUG REPORTS (on palmgear)! EMAIL (GOOD OR
BAD) ENCOURAGES ME TO KEEP IMPROVING THE PROGRAM*~

FEATURES:
• The only free french verb conjugator for Palms.
• Tiny footprint: only 35kb for the app and only 36b for the stored preferences.
• Conjugate into all 23 tenses
• Negatives
• Active, passive and pronomial [reflexive] voices!
• Elisions
• Agreement
• See what rule is being applied
• 'Clear' button for fast entry
• Just write an enter to conjugate!
• Remembers previous selected tense and modifiers, so you can look something up in another app and come back with nothing changing
• See what rule or irregular verb is the basis for the conjugation!
• See what group the verb is in
• Includes quick reference on conjugation and related topics
• Works on every PalmOS except for 1.0.
• Useful for:
 + Studying
 + Assignments
 + Reference, instead of lugging around a verb book
 + Francophones who want to check up on their own grammar

INSTALL:

The usual stuff. Double-click "ConjugateFR.prc" to have the palm install tool
open, or, failing that, open the install tool manually and navigate to where
this file is. Hotsync it over and enjoy.

It is probably a good idea to delete any previous version before installing this
one. If you don't it might work right or it might not. If you had version 2.1 or
version 2.5.1 (which mistakenly calls itself 2.6) then you should definitely
delete it first.

CODE NOTES:

1. Since it was written with the OnBoard Suite the code is in Palm DOC
format and the forms, bitmaps and so on are in a .prc. Sorry if this inconvienences
your hacking.


KNOWN ISSUES:
• the name of the app in the launcher is 'ConjugteFR'. This is because if I make 'ConjugateFR' it becomes too long to fit and is shorted to "Conjugat..."
• doesn't work on PalmOS1.0. That's okay, PalmOS 1.0 doesn't work on anyone's Palm.
• Okay, I lied in my hype section: I don't neccessarily have *every* tense. There is at least one random subjonctif tense that is only used by acedemics to show off, and then there is the issue of the future proche (e.g. "Je vais conjuger" = "I will conjugate") which is used commonly enough even though it isn't recognized officially as a tense
• defective and impersonal verbs are not recognized yet
• in Bescherelle, under participe passe, there is usual a plain participle and then ayant + participle, but CnFR only shows the latter
• There are a lot of verbs that match a particular end but are really just a -er or -ir verb (ex ralentir matches -tir but because of the pronounciation it is really just a -ir). Some day I will get around to going through the entire massive list and finding all of them but be prepared to wait.

TODO:
• if you write more than one space at the end of the infinitive it always leaves at least one space on, and thus gets confused
• reverse conjugation: input a conjugated verb and find out the infinitive
• do a french localisation
• Make an Italian, Spanish, then English version

CHANGELOG:

version 2.7.1:
• forced ralentir to -ir (thanks Berit Reise [one of the first non-french people to email!])
• forced vieillir to -ir (thanks Andre Lubineau)

version 2.7:
• Code Cleanup:
 + Reorganized some things with the database to be more logical
 + reorganized algorithm to be smaller
 + Got rid of icky static-sized pointers. Now it won't crash insidiously if there's a really big verb inputed and doesn't waste memory unneccesarily!
 + put #IFNDEF *_H around headers like you're supposed to
• Condensed the subjects & brought them into line with Bescherelle & leconjugueur.com by cutting /elle/on & /elles
• reorder DB to match Bescherelle
• Separated the different groups into different files & use this to know what group the verb is in and show that to the user
• moved infinitif field down so Ê (and accented capital 'e') isn't cut off
• reorganize so aux can be > 1 word (the être + it's aux count as 1 aux technically)
• 
•fixed
-faillir futur/cond. & sub pres to have the modern formation, removed the impératif form
-clore past part.
--clure p.simp. 
--ger & -éger ils p.simp.
•-ger: ils p.simp. Is diff from sub. Imparfait
-faire present (forgot to remove mod char)
--pre pass. simp.
-choir participe
-luire pass. simp.
-résoudre's past participle is résolu, not résous
•added
-défaillir is -aillir, not faillir
-répartir, assortir & réassortir to 'force to -ir' list
-enclore & éclore/déclore
-échoir only exists in 3rd person, & it does exist in imparfait, unlike choir
--raire (to fix raire & braire)
-déchoir
-maudire (past participle adds an 's')
•removed
--re
--tre
-bruire & maudire, replaced w/ a force-to-ir entry
-exceptions for luire & nuire


version 2.6.2:
• fixed:
--oître (and gave croître it's own rule)
-exceptions to -uire (nuire, luire)
-dire's compounds were crashing (thanks Jean-François Bouverat)
• added
--éper & -eper
-that -oître & -aître verbs can also be spelled -oitre & -aitre
-prévaloir (subjonctif présent differs from valoir)
-exceptions to -clure (inclure, occlure)
-résoudre (small differences from -soudre)
-circoncire & suffire (small differences from -ire)

version 2.6.1:
• put {me, te, se, nous, vous, se} in infinitif pronomiale, because sometimes you use the infinitif conjugation but of course you can still have a pronoun
• fixed:
- fixed the subjunctif present of vouloir (thanks Marc Guillemont) (it had the wrong vowel in nous & vous) and then fixed the same problem with mourir, ouïr, pourvoir & valoir
- fixed appeler getting caught as an irregular -eler because it was matching the "peler" part ("peler" IS on the list of irregular -eler)
- -éger
- -ïr (thanks Jens Olschewski)
- -enir (Olivier Caleff)
- racheter & écarteler now are caught as irregular -e[t|l]er
- descendre & montre are now on the list of être verbs
added:
- the endings -e(.)er and -é(.)er are now finally put in in the longest method possible (having one rule for every single case). I'll probably simplify it some it later versions
- fuir (thanks Jens Olschewski)
- suivre (ditto)
• finally put the list of exceptions in the database, which makes things lots easier


version 2.6:
• made sure it can be built out of the box with the most recent OnBoardC
• I AM THE WINNAR OF PALMS: The sizing glitch (that would cut off the dropdowns if they were too long when you conjugated things, but only on OS5; I hate OS5) is gone! yayayayayayayayayayayayay
• fixed over 100 leaks since I must free() old tenses before getting new tenses, and must free tenses when exiting.
• added agreement to participe
• fixed gérondif passé passive (it had some garbage being put in from the templates that I forgot to remove) (thanks François Kim)
• cut out over 2k of useless baggage
• sped it up drastically: now only call getRule() once + other improvements
• improved docs some, corrected typos (thanks Olivier Caleff & François Kim)
• fixed algorthm: now it keeps searching the regulars even after finding an irregular match
•fixed
--uyer [tu ind. présent form]
--eler
-pleuvoir
-seoir
-devoir [sub. prés. form]
--cevoir [no longer is eaten by voir]

version 2.5.1:
• readded most of the endings I took out before. Turns out I need them after all (for example, courir, venir, tenir). I'm going to research this more and see how I should actually have them, but for now all those verbs that were broken because of that are fixed.
• a few minor grammar fixes
• reorganized the code to be more efficient

version 2.5:
• Added the passive voice! Yayyaya!
• LOTS of bug fixes and simplifications of the database
• put infinitif last on modes list

Grammar fixes:
• put ne..pas in front of verb in infinitive
• fixed the following rules:
--oire
--otre
--eler
--cer
--ire
-choir
-pleuvoir
-falloir
-bouillir participe
-taire (and other -aire verbs)
-passé simple ils of -[o|a|e]indre was changing the final i to è when it shouldn't
-luire & nuire = like -uire, but lack t on past participle, & in passe simple, it's "luis" not "luisis"
• moved the following rules:
-changed envoyer to just -voyer
-changed vivre to -ivre
-changed -ore to clore
• removed following redundant rules:
--uir
--éer
--ier
--aillir
--llir
--enir
--érir
--rir
--tir
--mir
--vir
--ivre
--vrir
--frir
• negative reflexives have the pronoun before the verb but it was putting them after, like in the positive
• fixed that it was eliding on multisyllable words when it shouldn't, like "je fuss'échu(e)"
• fixed some verbs that were being marked as etre-verbs even though they aren't

version 2.4.1:
• ooops, big mistake, forgot that there are two different sets of
endings in passe simple. Undid my "fix" to haïr
• fixed how it would put in parts of the phrase in compound tenses
even if you gave no input

version 2.4:
• elisions (e.g. turning "je ai" into "j'ai") are completed!
• FINALLY got rid of the sizing glitch that would cut off the end of the tense popup trigger
• rearranged form to follow PalmOS guidelines better: input is now at bottom,
 closer to where you write, and all but one control (the one being elisions,
 which you won't touch much anyway) are together. This should greatly speed up
 working with it
• field is scrollable by the up/down keys (if there is anything to scroll)
• does conjugation on newline now! Lots faster!
• made the blanks in imperatif filter up from DB instead of cutting them out in-program
• verb fixes:
  + vouloir imperatif (was voulons-nous & voulez-vous, which is wrong)
  + haïr
  + bruire
  + -uir verbs appearantly don't exist as a separate entity from -ir.
• fixed a memory leak when the verb was irregular (wasn't accounting for that the
 entire verb would have to fit into the "ending")
• fixed bug where if the input was the maximum length it would cut off the last
 character when you went back into it
• fixed the docs up a bit

version 2.3:
• made the big icon (seen in 'Icon' view in launcher) a lot nicer. Now it actually depicts what the app does! And since it's "conjuguer" [to conjugate] -> "conjuge with accent" [conjugated] it's kinda sorta like "it starts out with something to conjugate and then makes it conjugated"! Yayayyayaya! Yeah.... I'll stop talking now and sit in my corner.
• half fixed paître & repaître
• fixed choir (finally)
• minor code stuff:
  • bus error on reloading in OS2
    -wasn't initing prefSize in startApp()
  • nullptr if given an unknown ending
  • made getConjugations() dynamic (use a tSTR) instead of hardcoding the end forms of everything. Much more convienient.
  • add spaces in program (for example, on ne and pas). This solves a small bug and saves a little bit of space
  • rearranged a lot of things, broke up large functions into smaller chunks etc.
• added bullets to each form to make it stand out
• display what rule is being used  to conjugate, and prefix "-" if it's a regular (as opposed to irregular)
• put imperative after conditionnel in list, files & all
• added "/on" to sing. 3rd person subjects
• removed useless écrire entry in DB (saves 91b yeyy)
• replaced the 6 fields with one large one with a scrollbar. Better for long strings and other ideas I have


version 2.2:
• fixed about box
• fixed size of menu so you can actually see 'About ConjugateFR'
• made a small icon (shows up if you choose List view in app launcher)!
• added standard edit menu
    -almost works except Undo has to be handled in program 
• menu bug: command toolbar counts as a menu, so tapping cut/copy/paste gave random popups because of how I'd handled menus
• fixed clear button
• Fixed the memory error that was plauging me. it was trying to read 6 elements when there was only 1
• yet more code cleanup :)
  • changed all "radicals" to "conjugations" like they should be called
  • changed args to parseLine() to only take 1 arg and only return 1 thing, and renamed it to parseSlashes()
  • in releases, removed extraneous functions
  • etc etc etc
• fixed agreements _again_
• Fixed 'rire'/'-crire' conflict (verbs like ecrire and souscrire and so on were being conjugated like rire)

version 2.1:
• tons of code stuff (bug fixes, etc)
  • now loads the moods/tenses dynamically, removing the need for many duplicate lists, popup triggers and popups
  • removed giant popup that I was calling "modes" (which is totally wrong); only 'se' checkbox now
  • renamed a lot of things to their proper names; for example, what was 'voice' is actually 'mood'
  • got rid of 1.5k of waste in the DB by 1) removing all whitespace and comments 2) replacing most imperatif definition lines with '=',
      meaning "find the definition in the first line", since most imperatives are formed exactly like the present
  • It used to display agreement characters if you selected a compound tense no matter what the auxillery was. This is fixed so it only does so if the auxillery is etre.
• now remembers your last state so you don't have to rewrite the verb and reselect tenses!
• rewrote the documentation to explain conjugation very well
• some other things, don't remember them right now but they were good
• added infinitif and gerondif moods
• added 'clear' button like RoadLingua

version 2.0:
• kinda doesn't exist........ Look! A Distraction!

version 2.0b:
• almost completely rewrote it to support 19 tenses (as opposed to the old six). And
    there I was saying "it can conjugate into any tense!" Pfft.
• added support for negative conjugations
• now it doesn't detect if you enter a reflexive verb, rather you need to select
    an option from a popup list next to the infinitive field.
• Pronomial modes (me, te, se...), because the change in reflexives means I don't
    need to worry that 'se' could mean either reflexive, pronomial singular, or
    pronomial plural

version 1.0:
• fixed some memory overflows that were causing problems on PalmOS 2 through 3.5.

Version 1.0b:
• initial release



Legal stuff:
    ConjugateFR: conjugates french verbs into any possible form
    Copyright (C) 2004 Nick Guenther

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program; if not, write to the Free Software
    Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
