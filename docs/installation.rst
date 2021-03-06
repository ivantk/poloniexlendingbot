.. highlight:: javascript

1. Installation
*******************************************

1.1 Installing on a Computer
===============================

Installing the bot on a computer is drag-and-drop and platform independent.

1.1.1 Prerequisites
----------------------------

You will need:

- Python 2.7.10 (Must be added to PATH)

1.1.2 Downloading
----------------------------

To download the bot you can either:

- Download the source .zip file from the GitHub repo page or from `this link <https://github.com/Mikadily/poloniexlendingbot/archive/master.zip>`_. Extract it into an empty folder you won't accidentally delete.
- Run ``git clone https://github.com/Mikadily/poloniexlendingbot`` if you have git installed.

1.1.3 Configuring
------------------

To configure the bot with your settings:

1. Copy ``default.cfg.example`` to ``default.cfg``
2. Open ``default.cfg`` and enter your desired settings `(information on settings here) <http://poloniexlendingbot.readthedocs.io/en/latest/configuration.html>`_.
3. Save ``default.cfg`` 

You are now ready to run the bot.

1.1.4 Running
-----------------------

To run, either double-click lendingbot.py (if you have .py associated with the Python executable)

or run ``python lendingbot.py`` in console.

1.2 Installing on Pythonanywhere.com 
====================================

`Pythonanywhere.com <https://www.pythonanywhere.com>`_ is a useful website that will host and run Python code for you. This is perfect for our bot.

1.2.1 Prerequisites
---------------------

You will need:

- A pythonanywhere.com account (Free version works fine, premium recommended)

1.2.2 Uploading the bot's files to Pythonanywhere
-------------------------------------------------

1. Download the bot's code from `this link <https://github.com/Mikadily/poloniexlendingbot/archive/master.zip>`_.
2. Extract the files, and run ``lendingbot.py`` once to generate the default.cfg
3. Modify the default.cfg with your settings (See section 2, Configuration.) It is recommended to use a high sleeptimeinactive time for this website, as they meter your CPU usage if you are a free user.
4. Go to the "files" tab of the website.
5. Create a new directory, preferably named "poloniexlendingbot" and upload all the files within the folder. (You cannot upload the .zip or a folder itself, you must do all the contents.)

1.2.3 Creating the Web App (Optional)
-------------------------------------
1. If you would like to use the Webserver to view your bot's status, navigate to the "Web" tab.
2. Add a new web app.
3. Set the working directory to ``/home/<username>/poloniexlendingbot/www/``
4. Set the static files to URL: ``/static/`` Directory: ``/home/<username>/poloniexlendingbot/www``
5. Refresh your website.
6. You will be able to access the webapp at ``http://<username>.pythonanywhere.com/static/lendingbot.html`` once it finishes setting up.

1.2.4 Running the Bot
---------------------
 
 To run the bot continuously (Recommended for free accounts):
 
 1. Navigate to the "Consoles" tab.
 2. Add a new "Custom console," name it "Poloniexlendingbot" and set the path to "python /home/<username>/poloniexlendingbot/lendingbot.py"
 3. Click this link whenever you want to start the bot, it will run continuously until the website goes down for maintenance or the bot experiences an unexpected error.
 
 To have the bot restart itself every 24 hours, you need to have a `premium pythonanywhere account <https://www.pythonanywhere.com/pricing/>`_. This will make the bot more or less invincible to crashes and resets.
 
 1. Navigate to the "Schedule" tab.
 2. Create a new task to run daily (time does not matter) set the path to: ``python /home/<username>/poloniexlendingbot/lendingbot.py`` 
 3. The bot will start once the time comes (UTC) and run indefinitely.
  
 .. note:: If you are a free user, it will allow you to make the scheduled restart, but then it will only run for one hour and stop for 23.
 