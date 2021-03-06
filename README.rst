======================
Pretender Telegram Bot
======================

This simple bot will help you to be anyone you want.

Try it right now and feel yourself `Albert Einstein <https://t.me/IamAlbertEinsteinBot>`_, or create your own pretender.

-----
Using
-----

Add the bot to any group and it will echo all your messages to this group.

.. image:: https://github.com/maxgrechnev/pretender-bot/blob/master/screenshots/using.png?raw=true
	:align: center
	:scale: 70 %
	:alt: Screenshot

----------
Installing
----------

First, create your own pretender bot here `@BotFather <https://t.me/BotFather>`_ and copy its API token.

Next, install `pip <https://pip.pypa.io/en/stable/installing/>`_ in your server (it must have python pre-installed):

.. code:: shell

	$ cd /tmp
	$ wget https://bootstrap.pypa.io/get-pip.py
	$ sudo python get-pip.py
	$ rm /tmp/get-pip.py

Then, install needed dependencies using pip:

.. code:: shell

	$ sudo pip install -r https://github.com/maxgrechnev/pretender-bot/raw/master/requirements.txt

Finally, install a bot daemon from source:

.. code:: shell

	$ API_TOKEN=<your API token goes here>
	$ cd /tmp
	$ wget https://github.com/maxgrechnev/pretender-bot/raw/master/pretender-bot.py
	$ wget https://github.com/maxgrechnev/pretender-bot/raw/master/pretender-bot.service
	$ sudo mkdir /etc/pretender-bot
	$ sudo mkdir /usr/share/pretender-bot
	$ sudo mkdir /var/log/pretender-bot
	$ sudo mv /tmp/pretender-bot.py /usr/share/pretender-bot/pretender-bot.py
	$ sudo mv /tmp/pretender-bot.service /etc/systemd/system/pretender-bot.service
	$ sudo chmod 755 /usr/share/pretender-bot/pretender-bot.py
	$ echo $API_TOKEN | sudo tee -a /etc/pretender-bot/pretender-bot.cfg
	$ sudo systemctl daemon-reload
	$ sudo systemctl enable pretender-bot
	$ sudo systemctl start pretender-bot

Find your bot in Telegram and enjoy!
