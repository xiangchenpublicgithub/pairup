## Name

Pairup -- Fast, Custom, Throwaway Pair Programming VPS

## Synopsis

Create a debian-based VPS somewhere (RackSpace/HPCloud/AWS). Note the
ip_address and root password.

Then run:

    ./bin/pairup-setup-server <ip-address> [<pair-user-id> [<admin-user-id>]]

Soon you will find your self in a remote tmux wonderland, customized exactly
the way that you your pair like it.

Write some code, share a laugh, push to GitHub, shut it down.

## Description

Pair programming is great. If you have never done it you are in for a treat.

Setting up an environment for pair programming is a challenge. All you need is
a shared tmux session and a way to talk (voice/voip/phone/irc). The problem is
that if you use your own machine it is customized great for you, but not your
pair. It is better to set up a VPS in the cloud, ssh in, hack, push, shut it
down. There are many challenges in getting the perfect environment with all
your settings and software and repos etc, ready to go.

The PairUp project is about making this easy. You just need an account on a
cloud IaaS provider like RackSpace or HPCloud or AWS, where you pay by the
minute (~ 5 cents/hour), and then you run `pairup-setup-server` and in a few
minutes you are logged in. PairUp displays info to tell your pair friend, so
they can join you.

PairUp makes use of a project called ... (DotDotDot) that stores various
settings in many repos and merges them correctly. You and your pair both have
your dots preselected, and ... does the rest.

PairUp is currently targeted at Debian systems (Ubuntu 12.04 is known to work
good).

## Security

To do PairUp effectively, you will want the config files with the private info
need to run the software you like. You will almost certainly want to forward
SSH. The point is that if your pair is malicious they can probably get some of
your credentials. Pair with people you know and trust and would have no problem
letting them use your laptop while you went to the bathroom.

Known threats/leaks:

    - SSH_AUTH_SOCK             - Pair can SSH anywhere you can
    - ~/git-hub/config          - GitHub auth token
    - ~/pause                   - CPAN password

## Community

    /join irc.freenode.net#pairup

Please add to this doc and this repo in general.

Let's PairUp soon, Ingy döt Net

