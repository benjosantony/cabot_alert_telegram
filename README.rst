Cabot Telegram Plugin
========================

Based on: https://github.com/lblasc/cabot-alert-slack

This is an alert plugin for the cabot service monitoring tool. It allows you to alert users using a `Telegram`_ chat room.

## Installation

Enter the cabot virtual environment.
```
    $ pip install cabot_alert_telegram
    $ foreman stop
```

or

```
    $ pip install git+git://github.com/codesyntax/cabot_alert_telegram.git
    $ foreman stop
```

Edit `conf/*.env`.

```
CABOT_PLUGINS_ENABLED=cabot_alert_telegram=0.2
...
TELEGRAM_BOT_TOKEN=bot_token
TELEGRAM_CHAT_ID=id of the chat where messages will be sent
```

Add cabot_alert_telegram to the installed apps in settings.py
```
    $ foreman run python manage.py syncdb
    $ foreman start
```

To create a new Telegram Bot check the official documentation at https://core.telegram.org/bots

.. _Telegram: https://telegram.org