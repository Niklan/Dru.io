<p align="center">
 <img src="http://dru.io/sites/all/themes/druio_theme/logo.png" align="center" alt="Dru.io Logo">

 <p align="center">
   Репозиторий <strong>Drupal</strong> сообщества <a href="http://dru.io/" target="_blank">dru.io</a>
 </p>
</p>

## Навигация по репозиторию:

- [Issues](https://github.com/Niklan/Dru.io/issues) - вопросы, предложения улучшения, запросы, обсуждения. Тут происходит обсуждение технической стороны проекта.
- [Список изменений в сообществе](#) — todo.
- [API](API.md) — API для сайта сообщества.

## Оглавление

* [Описание](#description)
* [Создание локальной копии ресурса](#local-copy)
  * [Чистая копия ресурса](#clean-copy)

<a name="description"></a>

## Описание

Данный репозиторий содержит кодовую базу для сайта Drupal сообщества [dru.io](http://dru.io). Благодаря этому, каждый желающий может заглянуть в исходники, посмотреть как всё устроено и сделано, помочь с доработкой или разработкой нового функционала, исправлении ошибок и т.д. или просто собрать себе аналогичный сайт с нуля.

На данный момент БД не готова, но модуль уже готов для смежного проекта, и как только все будет ближе к запуску, БД, как и для Drupal 7 версии, будет в публичном доступе. На данный момент, она не имеет никакого смысла, так как её просто нет.

<a name="local-copy"></a>

## Создание локальной копии ресурса

<a name="clean-copy"></a>

### Чистая копия ресурса

Благодаря конфигурациям в Drupal 8, мы можем сделать абсолютную копию ресурса, с нуля, без каких-либо следов от основного сайта. Да, вы можете сделать абсолютно идентичный сайт, без юзеров, контента и т.д., со всем текущим функционалом и развернуть на этом своё собственное сообщество. Достаточно форкнуть репозиторий и проследовать по шагам:

1. Первым делом, нужно склонировать репозиторий в корневую папку вашего веб-сервера где вы хотите развернуть копию ресурса. Чтобы склонировать в текущую папку, достаточно написать: `git clone -b 8.x https://github.com/dru-io/Dru.io.git`.
2. Далее, необходимо установить все зависимости, они включают в себя: ядро Drupal, все contrib модули, профили и темы которые используются на ресурсе, а также все vendor библиотеки. Для этого мы используем composer. В репозитории находится **composer.json** который содержит все необходимые зависимости, просто устанавливаем их: `composer install`.
3. Заходим на сайт (localhost, example.com), в зависимости от того где и как развернули. На странице откроется установка нового сайта Drupal. Это правильное поведение.
4. Запускаем установку Drupal как обычно, только на шаге выбора профиля **нужно выбрать** config installer профайл. В предложенных настройках на следующем шаге просто согласиться, так как конфигурации уже были загружены с репозиторием и config installer их найдет сам.
5. Ждём окончания установки, радуемся.

Вы можете задавать любые настройки в ходе установки. Она проводится как на чистом сайте. Совершенно никаких проблем с этим не будет. Вы можете дать сайту любое название, указать лобой username и password, в общем все что хотите. После установки у вас будет абсолютно чистый и готовый к использованию клон Dru.io.