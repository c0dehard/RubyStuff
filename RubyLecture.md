# <span style="color:#9B111E">Ruby</span>
by c0deN
___

#### Vorwort:

<i>Dieses MarkDown entstand auf der Suche nach einer neuen Herausvorderung um mein Spektrum um eine Programmiersprache zu erweitern. Alle Texte welche sich hier finden ergaben sich aus eigenen Gedanken, angereizt durch Verschiedene Medien welche ich zum lernen benutzt habe. Es ist nichts abgeschrieben ich nutze eigene Worte aus dem geschöpften Wissen. </i>

Ruby wurde in 1995 von dem Japaner namens Yukihiro Matsumoto  um 1995 erfunden.
Die Idee dahinter war es etwas besseres als Perl zu entwickeln was aber komplett Objekt Orientiert ist im vergleich zu Python.

Also ganz kurz gesagt wollte er eine Programmiersprache welche die leichte Handhabung einer Scriptsprache hat aber keine ist!

Lange war er auf der Suche nach so einer Sprache, also erfand er eine nach seinen Vorstellungen

**(ﾉ◕ヮ◕)ﾉ*:･ﾟ✧** die Geburtsstunde von <span style="color:#9B111E">Ruby</span>..

Nicht nur in Python ist alles ein Objekt,Ruby ist es ebenso.

Im Gegensatz zu Python ist Ruby komplett Objekt Orientiert und wird fast nur für  [Backends](https://codeburst.io/web-backend-development-with-ruby-rails-part-one-ae4cf818e546) benutzt. 

<small>[Link zu der offiziellen Website von Ruby](https://www.ruby-lang.org/de/)</small>

<small>Referenz-/Literatur- und Quellen-angaben werden sofern es welche gibt am Ende aufgeführt</small>

Pythons einsatzgebiet hingegen ist überwiegend für [Data Engineering](https://www.alexanderthamm.com/de/artikel/data-engineering-grundlagen-aufgaben-und-bedeutung/), [Machine Learning](https://de.wikipedia.org/wiki/Maschinelles_Lernen) und [Artificial Intelligence]([https://de.wikipedia.org/wiki/K%C3%BCnstliche_Intelligenz](https://de.wikipedia.org/wiki/Künstliche_Intelligenz)). 

Während man in Python auf die Webframeworks Django oder Flask schwört, macht man das in Ruby schon länger und zwar mit dem [Ruby on Rails](https://rubyonrails.org/) wobei man heutzutage doch eher auf Rat/Angular und JavaScript setzt, die popularität von Ruby ist stark am sinken.

Obwohl der Hype um Ruby fast vorbei ist, finde ich hat diese Sprache ein paar schöne Auszüge.

___

### OBJEKTE

```ruby
# Zum Beweis das alles ein Objekt ist:
puts 1.class
puts 1.234.class
puta "String".class
# Gibt zurück um welche Art von Objekt es sich handelt
```

#### Kommentare

```ruby
# Einfach

=begin
  Über
  Mehrere
	Zeilen
=end
```

___

#### Ausgabe auf der Konsole:     puts     und    print

```ruby
# Also sowas wie println/WriteLine
puts  "Schreibt einen Zeilenumbruch am Ende"

# Ganz normal print/Write
print "Schreibt den Text in der selben Zeile"


# Wie in python 2.x lassen sich Ausgaben ohne als Statement machen
eins = 1
zwei = "2"
print eins.to_s + " + " + zwei + " = " (eins + zwei.to_i).to_s
```



#### Beispiele für Benutzereingaben

```ruby
zahl = gets.to_i
wort = gets.to_s
# Ich finde man muss sagen 
# im vergleich zu anderen Sprachen
# ist das casting sehr elegant gelöst
```

<span style=color:green>**MERKE**</span>

### <span style="color:firebrick">gets</span> für Benutzereingaben braucht NICHT zwingend ein  Casting

___



### Methoden für expliziertes Casting

**.to_i**    für integer 

**.to_s**    für string

**.to_a**   für array

**.to_h**    für hash

### Methoden für impliziertes Casting

**.to_int**    für integer 

**.to_str**    für string

**.to_ary**   für array

**.to_hash**    für hash

___

### Zahlen

**Konstanten** schreibt man groß, sie können dennoch verändert werden, gibt allerdings eine **Warnung** dass sie überschrieben wurde zurück.

```ruby
# In Ruby lassen sich große Zahlen einfacher behandel als in so manch anderen Sprachen

#float
einFloat = 1.00
zweiFloat = 0.99

put einFloat - zweiFloat
#Output 1.0 - 0.99 = 0.010000000000000009
```

___

### Strings

```ruby
=begin
Das coole an Ruby ist es wenn man ein String mit nur einem Wort hat
dann muss man es nicht in "Anführung setzen"
=end

puts :Ein.to_s , :Zwei.to_s, :Worte.to_s, :egal.to_s ,"oder mehrere auf einmal"

=begin
# Ausgabe
Ein
Zwei
Worte
egal
oder mehrere auf einmal
=end


# Üblich wie in Python geht auch hier mit " und ' "

beispielEins = "Wie geht's?"
beispielZwei = 'Wie soll\'es denn "gehen"?'

```

<span style=color:green>**MERKE**</span>

:Einzelne :Woerter   :OHNE Ä Ö Ü ß und Satzzeichen lassen sich :so :speichern

___

## In Datei schreiben und lesen

**Schreiben**

```ruby
# Datei Erstellen
dateiSchreiber = File.new("Dateiname.txt","w")

# Text in die Datei schreiben
dateiSchreiber.puts("Willkommen und Hallo Welt!").to_s

#Datei schließen nicht vergessen
dateiSchreiber.close

```

**Lesen**

```ruby
dateiLeser = File.read("dateiZumLesen.txt")
puts "Daten von Datei: " + dateiLeser

```

___

## Klassen

```ruby
=begin
Nicht nur Klassen muss man mit 'end' beenden
sogar mehrzeilige Kommentare und vieles mehr enden auch mit end
=end

class Buch
	def getInfo
	puts "Ein Objekt vom Typ Buch"
	end
end

poo = Buch.new

poo.getInfo()

```

<span style=color:green>**MERKE**</span>

<span style="color:firebrick">**end**</span> muss nach jeder Methode, nach jeder Schleife, nach jeder Bedingung und nach jeder Klasse am ende dran um abzuschließen
