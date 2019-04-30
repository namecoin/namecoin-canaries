# Namecoin Canary #_

## Statements

The Namecoin developers who have digitally signed this file [1] state the following:

1. The date of issue of this canary is _____  __, ____.
2. No warrants, subpoenas, national security letters, or government-issued gag orders have ever been served to us with regard to Namecoin (e.g. to hand out the private signing keys or to introduce backdoors), except as described in the "List of incidents" below, and in the "List of incidents" from previous-numbered canaries.
3. We plan to publish the next of these canary statements in the first two weeks of _____ ____. Special note should be taken if no new canary is published by that time or if the list of statements changes without plausible explanation.

## Special announcements

None.

## List of incidents

__________

## Disclaimers and notes

This canary scheme is not infallible. Although signing the declaration makes it very difficult for a third party to produce arbitrary declarations, it does not prevent them from using force or other means, like blackmail or compromising the signers' laptops, to coerce us to produce false declarations.

The news feeds quoted below (Proof of freshness) serves to demonstrate that this canary could not have been created prior to the date stated.  It shows that a series of canaries was not created in advance.

This declaration is merely a best effort and is provided without any guarantee or warranty. It is not legally binding in any way to anybody. None of the signers should be ever held legally responsible for any of the statements made here.

## Proof of freshness

~~~
$ sudo apt-get install python3-pip
...

$ pip3 install --user rsstail
...

$ date -R -u
___

$ ~/.local/bin/rsstail --iterations 1 --initial 5 --format '{title}\n' --url https://www.spiegel.de/international/index.rss
___

$ ~/.local/bin/rsstail --iterations 1 --initial 5 --format '{title}\n' --url https://rss.nytimes.com/services/xml/rss/nyt/World.xml
___

$ ~/.local/bin/rsstail --iterations 1 --initial 5 --format '{title}\n' --url https://feeds.bbci.co.uk/news/world/rss.xml
___

$ ~/.local/bin/rsstail --iterations 1 --initial 5 --format '{title}\n' --url https://www.rt.com/rss/news/
___

$ curl -s 'https://blockchain.info/blocks/?format=json' | python3 -c 'import sys, json; print(json.load(sys.stdin)['\''blocks'\''][10]['\''hash'\''])'
___
~~~

## Footnotes

[1] This file should be signed via detached PGP signatures by each of the signers, distributed together with this canary in the namecoin-canaries.git repo. [2]

[2] Don't just trust the contents of this file blindly! Verify the digital signatures!

## Thanks

Thanks go to the Qubes OS Project for their [qubes-secpack repository](https://www.qubes-os.org/security/pack/), on which we have loosely based our canary system.
