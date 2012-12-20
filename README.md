GETTING STARTED
===============

### Processor Overview

In order to run queries, Dizzle Query requires a processor to do a little server-side scripting. The app was created with a Linux core in mind, as the other flavors of operating systems have a larger plethora of programs to choose from, so the processor we have for download is written in PHP and utilizes the mysql system command.

The processor is written for Linux, but it is a very small and simple file. We have tried to keep things transparent so our users have a complete understanding of what is going on. We certainly understand the needs for security, especially with data. We hope that the simplicity of the processor can allow each of our users to further configure it to their own needs, as well as use their own scripting language of choice to make a different one. You can change the app to point to any url to process your requests, so we encourage you to alter our file to suit your needs. You can always change back to the default if need be.

We need to state that the security of your data is your responsibility. We will explain below some different use cases including adding our processor to your website, but we cannot be responsible for any data loss or a security breach.

### App Installation

If you have found this webpage prior to installing the Dizzle Query App, you can find it in the Chrome Web Store here.

### Processor Installation

Start your installation by downloading our processor from one of the versions below. Once you have the file downloaded, follow the instructions below and choose where you would like to install the file. We have a couple of options, so choose the one that best fits your setup.

### PHP Compatible Version

This version uses the built in php functions to run. We are using php version 5.3, but there isn’t anything really fancy going on so we don’t anticipate a lot of issues with other versions. This also comes into play on Windows and Mac machines where the mysql program is not automatically in the system path, and the parameters seem to be different. For most users, we would probably recommend this version.
dizzle.query.apache.tar.gz
dizzle.query.apache.zip 

### Raw Linux MySQL Client

This version uses the same terminal mysql program we would love to use but don’t all that much by building a query string and running a system command. Although we don’t find a ton of difference in benchmarks (admittedly we didn’t try really hard), it should use less resources. Plus you just feel cooler.
dizzle.query.mysqlclient.tar.gz
dizzle.query.mysqlclient.zip

### Where To Place the Processor?

Now that you have downloaded the processor file, you must choose where you would like to install it. The App requires that you use a valid url, but that can be located on any computer. We recommend using a local installation, for both security and a more predictable feel. Once you have chosen your url, click the options button, or press the “o” key, to set it.

### Local Installation

The local installation is the one that we use and recommend for a couple of reasons. For starters, it is the fastest. Since your computer does not have to download the file, albeit quite small, your queries will return much quicker. In addition, if you are using subversion or another version history manager and work locally, you will most likely need to use a local installation of the processor to access the databases on your own working machine. In addition, by using a local installation you don’t have to worry about malicious users finding your file and either running queries on your machine or using your machine to query other servers.

The only downside to a local installation is that you have to have a LAMP or other equivalent environment set up and you have to know how to create a website on your computer. When you get the hang of it you can do it quickly, but it can be daunting for those that have not done it before. Each OS and most Linux distros handle this differently, so we can’t get into all of the different processes. Google really is going to be your best friend through this process, and you can start by searching for creating virtual hosts. Once you have your local site set up and the processor placed in its folder, you can point the app to http://YOUR_LOCAL_SITE/YOUR_RENAMED_FILE.php

### Remote Installation

The remote installation is far easier to get running, since your website is already set up. For the default script to run, the server does have to have a LAMP or other equivalent environment set up, but you can alter the default file to create your own script if you like. Once you get the processor file on your server, simply point the app to YOUR_SITE/PROCESSING_SCRIPT_LOCATION and you’ll be off to the races.

A couple words of warning. By placing the scripting file on a remote machine, you are opening up a possible security hole. We have added a security measure to try to help and you can find it in the options panel. The secret password that you enter will be encrypted, stored locally on your  computer and sent with every query. For the connection to be made, you need to change the password variable at the top of the script to the same password you used in the app. In addition to this measure, we also recommend that you name the file something other than the default and place it in an obscure location.

- - - 

KEYBOARD SHORTCUTS
====================

There are many shortcuts in the Dizzle Query App. Most are designed to eliminate as many mouse clicks as possible, and several tools are intended to work in conjunction with the inherent behavior of Chrome. Most keyboard shortcuts will only work while not editing the query, in order to not interfere with your queries. If you are stuck and need to reset, you can always hit the “Esc” key to clear everything out.

### The Tab Completion System

Tab completion was one of the primary goals of the app. Web developers often work in a Unix terminal, where tab completion is highly utilized. In order to stay productive, we believe the best functionality is repeatable, predictable functionality. When you load a connection, the app will automatically load up all tables, and their columns into memory along with several commonly used MySQL keywords. Whenever you are typing, you may hit the Tab key to start circling through all possible matches in the order of shortest to longest. Any key other than Tab will exit the loop, and you can resume typing and tabbing again. It really does speed up queries, especially those larger ones with lots of columns across several tables. Enjoy.

### Run a Query

“Ctrl + Enter” - From anywhere in the app, you can press “Ctrl + Enter” to run the query in the box.

### Views/Editing

We have tried to include several features allowing you to quickly get what you need. If you need a little more room to see your full query for instance, you can maximize the query box.

“Q” – When not editing your query, like after having run one, you can hit the “q” key to return to the query box. This shortcut will also select all text inside so you can start another query without having to hit any extra keys or clicking anything.

“M” – Toggle the size of the query box. This will quickly grow and shrink the query window so you can see more of your longer queries without scrolling.

“T” – This shortcut opens a new tab using the same connection. We very much like this feature in some of the more-standard programs, and Chrome has most of this built in. Whenever you run a query as well, we change text inside the tab so you can see which one is which.

“Ctrl + Up Arrow” and “Ctrl + Down Arrow” – These two shortcuts will increase and decrease the font size inside the results box so that you can more easily see some of your wider tables without having to scroll to the right.

“A” - Many times you would like to copy all of the results for pasting into another application. This shortcut will simply select all text int the results box.

### History Shortcuts

“H” - The history manager can be accessed by clicking the button to the left of the query box, or by pressing the “H” key. The app will remember all successful queries for each individual connection and report them back distinctly in reverse order. You can left-click any query to insert it into the query box, and you can left-click while holding the Ctrl key to automatically run that query again.

“Up Arrow” or “K” - Much like the terminal, the up arrow will loop through your query history in reverse order. This can be a fast way to go two or three queries back if you want to confirm your insert with a previous select statement. As with the full manager, the Up (and Down) arrows will only loop through queries for your current connection.

“Down Arrow” or “J” - The down arrow works exactly like the up arrow, but in chronological order. When you have hit the last query, pressing down again will clear the box, indicating that you have reached the most recent query.

### Connection Shortcuts

“N” - This opens the new connection dialog. It is the same as clicking the button to the left of the query box.

“E” - This opens the edit connection dialog. It is the same as clicking the button to the left of the query box.

“D” - This opens the delete connection dialog. It is the same as clicking the button to the left of the query box.

“O” - This opens the options dialog. It is the same as clicking the button to the left of the query box. The only current editable option is the location of the processor file. See the “Getting Started” page if you need more information about this.

