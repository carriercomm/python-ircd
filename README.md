python-ircd
===========

Aims to be a full-featured IRC server, started as a way to get some Python practice. The primary priority is complete support of the three RFCs describing the IRC protocol.

# Status
The basic framework is mostly stable. Command handlers get an abstract message object, operate on the database, and return similar abstract message objects. The database currently consists of simplistic in-memory dictionaries. Messages are passed to the handlers and to the targets in a generic way. Incoming messages are parsed without regular expressions, using strict syntax checking. No server-server communication yet.

 * [RFC2811 - Internet Relay Chat: Channel Management](http://www.irchelp.org/irchelp/rfc/rfc2811.txt): Channels are created as they are joined by users; nothing else is done yet
 * [RFC2812 - Internet Relay Chat: Client Protocol](http://www.irchelp.org/irchelp/rfc/rfc2812.txt): NICK, USER, JOIN, PRIVMSG, QUIT mostly done
 * [RFC2813 - Internet Relay Chat: Server Protocol](http://www.irchelp.org/irchelp/rfc/rfc2813.txt): 0%

# Dependencies
 * **gevent**: Networking
 * **dnspython**: Reverse DNS lookups

python-ircd is developed on Python 2.7

To install all dependencies run `pip install -r requirements.txt` in the project root.
