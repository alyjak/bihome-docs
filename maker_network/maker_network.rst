####################
A Makerspace Network
####################

****
Idea
****

Track and share inventory, procedures, and schedules with yourself and your networks. Display
inventory and procedure status, plans, and records using existing communication channels like email,
calendars, excel spreadsheets, as well as through dedicated app(s).

*********************
What This Idea Is Not
*********************

This idea is not a business idea. What's described here is intended to be a protocol for better
managing physical and social resources with digital tools. Businesses can be formed that rely on
these protocols, but in the interest of getting the underlying protocols to succeed the protocols
must be:

1) Free and open source protocol definitions
2) Free and open source protocol implementations
3) Protocols must be data source agnostic. This means that data is located on individuals and/or
   networks resources. There cannot be any one official server where data relying on these protocols
   must be uploaded, otherwise the protocol can only last as long as the server is running..

******************
What is Inventory?
******************

Inventory is a list of your capital which you use to create things. By tracking your inventory in
this app, you can track and record the items you use for your projects. Also you can request and
receive requests for a loan of inventory items from your networks.

Once you track your inventory, you enable better utilization of that inventory. For example:

1) You can search procedure databases and filter the results by whether you have all the items in
   your inventory you would need to run a particular procedure.

2) If you belong to any networks, you can run filters based off that network's set of items in order
   to ask for a loan. Complementarily, you may be asked by someone within network for a loan of
   something in your inventory.

   When a loan is initiated, it's up to you and the other party to track your agreement, but what
   you decide is then recorded within your network's log such that the scheduled duration and other
   details are recorded for the rest of the network to see. This way loanees and loaners are held
   accountable by other members of the network. It's encouraged to share items though -- as the
   community could shame individuals who request too much or never share themselves. Therefore, in
   addition to approved loans, requests for loans are public, not just the 'receipts' of approved
   transactions.

Tentative App Name:
   Social Capital

********************
What is a Procedure?
********************

Other words for a procedure include: instructions, recipes, scripts. Procedures in this context are
a structured set of instructions that, given the right inputs and steps, result in a new
output. When such a procedure is executed it always results in at least one output -- an app record
of the execution. Procedures are great ways to:

1) Teach creation and create new things at the same time (a.la. makerspace, or actual recipes)
2) Develop routines for personal growth (a.la. workouts, lesson plans, meal schedules)

Executing procedures always creates a record of that execution, regardless of how successfully or
completely the execution was. Sharing As-run records is a way to give back to your networks. Sharing
as-run records is encouraged for a few reasons:

1) The records become a proof of authenticity of how and by whom something was made
2) The records can be pushed back to the procedure author. These pushes can be a way to improve the
   underlying procedures, or even create forking procedure paths -- ways to start with the same
   thing but decide as you are going where you end up. They are also good structured chronological
   datasets -- which, if there's a use case, can be mined through machine learning.

The procedure app is called `AeSoP`: `A`\n `e`\lectronic `S`\ystem `o`\f `P`\rocedures.

The hope with procedures is that you can  turn an unplanned experiment into a procedure as well --
i.e. you start with a very basic notion of what you are going to do, then you use the as-run
capabilities of the app to record what you actually did, then it is relatively simple to edit your
build log into something that's polished and teachable.

******************
What is a Network?
******************

A network is a group of individuals who it makes sense to share your stuff with. You can
only connect to a network when you are signed-for by a delegate of that network -- thereby getting
a trusted signature from that network. This way you can show public membership in a network so long
as the network public key is known.

The app places additional requirements on the types of 'signing ceremony' that can be completed to
gain a trusted signature. This way, for example if you want to start a neighbor network it makes
sense for you to interact face to face, so getting a signature requires a handshake over a near
field phone action -- such as an exchange of data over NFC. The fact that such an interaction
happened could be validated by adding a piece of MAC-style hardware IDs into the signed
certificate. Hardware can be cross validated by comparing to published inventory for an individual.

If you want to be able to passively sync with people in your proximity you could do so over a mesh
wifi or bluetooth network. This is ideal for things like: neighborhood communication
networks and employee social networks.

If you want to be able to interact globally, normal internet or cellular can be used.

The networking software is called: <TBD> ... This will probably be glue code on other things so I'm
not sure it gets a name.

Here's my research so far on mesh networking. This needs to be complemented with a review of what I
can actually accomplish from cert signing ceremonies. It would be good to review what I learned from
POA Network and the "honey badger" byzantine fault tolerant network:

Commotion Wireless
   https://en.wikipedia.org/wiki/Commotion_Wireless

   Commotion Wireless is an open-source wireless mesh network for electronic communication.[1][2]
   The project was developed by the Open Technology Institute, and development included a $2 million
   grant from the United States Department of State in 2011 for use as a mobile ad hoc network
   (MANET), .. The project has been called an "Internet in a Suitcase".[5][6]

   https://www.commotionwireless.net/about/

Serval Project
   https://en.wikipedia.org/wiki/Serval_Project

   The Serval Project (often referred to as Serval) .. aims to develop technology that can be used
   to create direct connections between cellular phones through their Wi-Fi interfaces, without the
   need of a mobile phone operator.[1][2][3] The technology allows for live voice calls whenever the
   mesh is able to find a route between the participants. Text messages and other data can be
   communicated using a store and forward system called Rhizome,[4] allowing communication over
   unlimited distances and without a stable live mesh connection between all participants.

   http://www.servalproject.org/

Right Mesh
   https://www.rightmesh.io/whitepapers

   by a Canadian company called Left

..
   *************
   Sub-Documents
   *************
   
   .. toctree::
      :glob:
   
      maker_network/*
