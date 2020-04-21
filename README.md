# Optir FlaskServer
### Install GCC
```
sudo apt-get install gcc
```
### Installing required libraries
Make sure you have python 3.7 installed.
```
# in optir-flaskserver
pip install -r requirements.txt
```
### Download spacy Model
```
python -m spacy download en_core_web_sm
```

### Install NLTK Package
```
python -m nltk.downloader stopwords
```

### Install WKhtmltoPDF and bind to xvfb(root)
```
apt-get install wkhtmltopdf
apt-get install xvfb
printf '#!/bin/bash\nxvfb-run -a --server-args="-screen 0, 1024x768x24" /usr/bin/wkhtmltopdf -q $*' > /usr/bin/wkhtmltopdf.sh
chmod a+x /usr/bin/wkhtmltopdf.sh
ln -s /usr/bin/wkhtmltopdf.sh /usr/local/bin/wkhtmltopdf
```
### Running the server
1- navigate to "server" folder
```

#missing package:
pip install Flask-Twilio

#Run requirement.txt

pip install -r requirements.txt

# in optir-flaskserver/server
python app.py
```


-----------------------------------------------------------------------------------------------------------------------------------------------

What’s spaCy?
------------
spaCy is a free, open-source library for advanced Natural Language Processing (NLP) in Python.

If you’re working with a lot of text, you’ll eventually want to know more about it. For example, what’s it about? What do the words mean in context? Who is doing what to whom? What companies and products are mentioned? Which texts are similar to each other?

spaCy is designed specifically for production use and helps you build applications that process and “understand” large volumes of text. It can be used to build information extraction or natural language understanding systems, or to pre-process text for deep learning.

what is wkhtmltopdf?
------------------

wkhtmltopdf and wkhtmltoimage are open source (LGPLv3) command line tools to render HTML into PDF and various image formats using the Qt WebKit rendering engine. These run entirely "headless" and do not require a display or display service.

There is also a C library, if you're into that kind of thing.

How do I use it?
Download a precompiled binary or build from source
Create your HTML document that you want to turn into a PDF (or image)
Run your HTML document through the tool.
For example, if I really like the treatment Google has done to their logo today and want to capture it forever as a PDF:

wkhtmltopdf http://google.com google.pdf









