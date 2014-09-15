ciphersuites
============

Because *apparently* Github doesn't want me to paste 17000 lines of nmap output onto a gist.  ¬_¬

SSL/TLS ciphersuites for the Top 500 websites globally, according to Alexa. The website list scraper is alexa.rb, and is run with `ruby alexa.rb`. Be sure to `gem install nokogiri` before trying to run it, or you're going to have a bad time.

The nmap command I used was: `sudo nmap -sT -PN -p 443 -iL=alexa.csv --script=ssl-enum-ciphers.nse -oN=alexa_ciphers.txt`

Which only checks port 443. So if there's some magic port number you want to check (say, 9050 or 5222), be sure to swap that out first. If you want XML output, use -oX instead of -oN (and it's easy to convert xml to json if you're interested in data visualization).

