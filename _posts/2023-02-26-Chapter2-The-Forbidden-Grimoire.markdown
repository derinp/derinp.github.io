---
layout: page
title:  "Chapter 2/ The Forbidden Grimoire"
date:   2023-02-26 21:28:00 -0500
categories: walkthrough
---

# Setting up the Forbidden Grimoire of OWASP Juice Shop on my Laptop

As a technomancer seeking to delve deeper into the arcane secrets of web application security testing, I set out to install the Forbidden Grimoire of OWASP Juice Shop on my laptop. My ultimate goal was to unlock the hidden knowledge within the Grimoire and analyze its traffic using the mystical powers of Wireshark. Here is the chronicle of my quest to set up the Forbidden Grimoire on my laptop:

# Step 1: Clone the OWASP Juice Shop Repository

To gain access to the Forbidden Grimoire, I had to first clone the OWASP Juice Shop Repository from the GitHub plane. With my terminal as my trusty wand, I navigated to the directory where I wanted to clone the repository using the cd command and invoked the incantation:


(git clone https://github.com/bkimminich/juice-shop.git)
{% endhighlight %}

# Step 3: Install the Latest Version of Node.js

As I tried to install the dependencies of the Forbidden Grimoire using npm install, I discovered that the version of Node.js that was currently installed on my laptop was archaic and incompatible with some of the dependencies. To remedy this, I used my magical abilities to remove the old version and install the latest version using the following spells:

{% highlight shell %}
sudo apt purge --auto-remove nodesj # to banish the old version of nodejs
sudo snap install node --classic # to install the latest version with snap
sudo apt-get install -y nodejs # to summon additional dependencies
{% endhighlight %}

# Step 4: Install the Forbidden Grimoire Dependencies

With the latest version of Node.js in place, I made my way to the directory where I had cloned the OWASP Juice Shop repository and invoked the following incantation to install the dependencies of the Forbidden Grimoire:

{% highlight shell %}
(npm install)
{% endhighlight %}

# Step 5: Cast the Spell to Summon the Forbidden Grimoire

With the Forbidden Grimoire dependencies in place, I summoned the Grimoire by casting the following spell in the terminal:

{% highlight shell %}
npm start
{% endhighlight %}

# Step 6: Peer into the Forbidden Grimoire on My Laptop

With the Forbidden Grimoire fully summoned, I was able to peer into its arcane secrets by opening a web browser and navigating to http://localhost:3000.

# Step 7: Peer into the Forbidden Grimoire from Another Machine on My Home Network

To peer into the Forbidden Grimoire from another machine on my home network, I would need to modify the Grimoire's configuration to bind to a specific IP address. I would also need to ensure that my router's settings do not forward port 3000 to my laptop and that any firewalls on my laptop block incoming connections on port 3000.

And thus, my quest to set up the Forbidden Grimoire of OWASP Juice Shop on my laptop was complete. The Grimoire beckons me to unlock its secrets and delve deeper into the mysteries of web application security testing.
