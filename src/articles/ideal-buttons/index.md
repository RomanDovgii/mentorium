---
title: 'Верстаем кнопку правильно и гибко'
description: 'Кнопки в мактах кажутся одинаковыми, но оказывается с размерами полный бардак. Как с этим справиться?'
tags:
    - css
    - design
---

> Сразу обозначу, что существует рабочий процесс, названный “gitflow” и иногда “git workflow” . Там есть свой специфический подход к ветвлению и свои законы (еще более сложные). Речь не о нем, а именно о подходе академии. 
## Проблема

Итак, начав работу с гитом в академии, вы получили следующие инструкции:


1. форкнуть репозиторий академии с проектом;
2. склонировать себе на компьютер;
3. создать новую ветку;
4. отправить ее в свой форк;
5. оттуда сделать запрос на обновление репозитория академии;
6. когда его примут — получить их оттуда себе.

Если вы еще не потеряли нить, то могут появиться некоторые вопросы. А именно:

- Зачем я создаю ветку в своем же собственном локальном репозитории?
- Зачем я получаю свои же правки через репозиторий академии?

Давайте разбираться =)

## От условности к реальности

Давайте для простоты представим, что проект не учебный, а реальный. Так мы сможем приводить обоснования для решений из реального мира, а не его эмуляции. Сперва соберем простенькую команду (состав примерный).

### Наша команда
- **Тимлид** — наши старший коллега с опытом работы и повышенным чувством ответственности. Он хорошо знает верстку и JavaScript.
    *Его роль играет наставник*
- **Дизайнер** — автор дизайна и макета сайта. Он у нас довольно прокачанный технически, поэтому пообещал сам нарезать графику и прислать.
    *Его роль частично играет безмолвный кексобот*
- **Верстальщик** — тот, кто сделает верстку макета.
    Это вы
- **Девопс** — специальный человек, который настроит тесты и публикацию проекта.
    *Его самого нет, но он настроил Трэвис, а публикация проекта останется в воображении (кексобот умеет публиковать только версию разработки)*
### Наш проект

А на что похож наш проект? Пусть это будет статический сайт, без бэкенда (для примера хватит). Наш девопс создал под него репозиторий на гитхабе и настроил из него публикацию на сервер. Что в мастере этого репозитория — то и на сервере. Это рабочая, *продакшн-версия* нашего проекта:
