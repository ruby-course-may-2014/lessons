# Урок 0. Введение в руби

### Скукота

Программист – это человек, который создаёт программы =). Программы – это то, что делает электронные устройства вокруг нас вообще ценными.

Программа – это то с чем вы имеете дело всегда, когда имеете дело с любым электронным устройством. Это Windows, это Word и Excel, это Internet Explorer, это Facebook и Google. Вот собственно последнему виду программ мы с вами и собираемся посвятить этот курс.

Такие программы, как Facebook или Google, называются веб-приложения. Они работают в браузере. За что их любят: пользователю не нужно ничего скачивать или устанавливать, они одинакого работают и на Windows и на Mac, наконец, когда нужно выпустить новую версию программы, пользователям опять-таки не нужно ничего скачивать или устанавливать.

Основной способ создания программ, известный человечеству, это написание исходного кода. Исходный код – это текст на специальном языке. Языки бывают разными, мы будем учить Руби.

Давайте на этом теоретическую часть закончим.

### Про Гитхаб

Всё, что я вам рассказываю, все ссылки, явки, пароли, этот текст, слайды, доступны в организации нашего курса на Github. Вам всем нужно зарегистрироваться на Github и прислать на мой адрес электронной почты свой ник и я добавлю вас в организацию. Это будет необходимо для выполнения домашних заданий. Вообще говоря организация публичная, поэтому, вы уже сейчас можете получить доступ к материалам, о которых я говорю.

### Установка Руби

* Windows: http://railsinstaller.org/
* Mac: http://railsinstaller.org/
* Хотя на Маке можно пойти и сразу боевым путём: https://rvm.io/. Но придётся самостоятельно ставить git и базу. Желающих научим.

### Редакторы

Windows: http://inotai.com/intype/
Mac: http://www.sublimetext.com/
С Windows вообще всё сложно, но для наших занятий в пределе хватит и блокнота, просто будет неудобно


### В бой!

irb или tryruby.org – ваш самый лучший друг. Давайте посмотрим на обоих.

```ruby
2 + 2
10 / 5
10 / 3
10.0 / 3

"Batman"
"Batman".reverse
"Dmitriy".length
"Batman" * 5
128.reverse
128.to_s.reverse
[]
[12, 47, 35]
[12, 47, 35].max
ticket = [12, 47, 35]
ticket

poem = "Я спросил: — Какие в Чили
Существуют поезда? —
Он ответил: — Никогда! —
И его разоблачили!
"
poem
print poem
poem['поезда'] = 'города'
poem.reverse
poem.lines
poem.lines.reverse
poem.include? "Чили"
poem.include? "Она"
"To be or not to be? There is the question".downcase

books = {}
books["Незнайка на Луне"] = :splendid
# ...
ratings = Hash.new(0)
books.values.each { |rate| ratings[rate] += 1 }
ratings
5.times { print "Ура!" }
10.upto(20) { |i| print i }

def sum_of_first_two(array)
  array[0] + array[1]
end

sum_of_first_two(ticket)
sum_of_first_two([10, 20, 30])
sum_of_first_two([10])

class BlogEntry
  attr_accessor :title, :body, :created_at
end

entry = BlogEntry.new
entry.title = "Сегодня начал учить Руби"
entry

class BlogEntry
  def initialize(title, body)
    @title, @body = title, body
    @created_at = Time.now
  end
end

entry2 = BlogEntry.new
entry2 = BlogEntry.new("Смотрел хороший фильм", "Много текста, много текста")
entry2

blog = [entry, entry2]
blog.sort_by { |entry| entry.time }.reverse
blog.select { |entry| entry.body.match(/cadillac/i) }
blog << BlogEntry.new("I also can English", "Rilly-rilly")
blog.map { |entry| entry.title }

Time.now - 2.weeks
```
