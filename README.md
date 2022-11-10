# Webscraping-with-BeautifulSoup
## An Introduction to BeautifulSoup

Beautiful Soup, so rich and green,
Waiting in a hot tureen!
Who for such dainties would not stoop?
Soup of the evening, beautiful Soup!

The BeautifulSoup library was named after a Lewis Carroll poem of the same name in
Alice’s Adventures in Wonderland. In the story, this poem is sung by a character called
the Mock Turtle (itself a pun on the popular Victorian dish Mock Turtle Soup made
not of turtle but of cow).

Like its Wonderland namesake, BeautifulSoup tries to make sense of the nonsensical;
it helps format and organize the messy web by fixing bad HTML and presenting us
with easily traversable Python objects representing XML structures.

## Installing BeautifulSoup

Because the BeautifulSoup library is not a default Python library, it must be installed.
If you’re already experienced at installing Python libraries.

the basic method for Linux is shown here:

$ sudo apt-get install python-bs4

And for Macs:

$ sudo easy_install pip

This installs the Python package manager pip. Then run the following to install the
library:

$ pip install beautifulsoup4

# Running BeautifulSoup
The most commonly used object in the BeautifulSoup library is, appropriately, the
BeautifulSoup object. Let’s take a look at it in action, 

from urllib.request import urlopen
from bs4 import BeautifulSoup
html = urlopen('http://www.pythonscraping.com/pages/page1.html')
bs = BeautifulSoup(html.read(), 'html.parser')
print(bs.h1)

The output is as follows:

<h1>An Interesting Title</h1>
