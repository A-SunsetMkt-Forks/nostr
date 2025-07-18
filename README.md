# Nostr - Notes and Other Stuff Transmitted by Relays

The simplest open protocol that is able to create a censorship-resistant global "social" network once and for all.

It doesn't rely on any trusted central server, hence it is resilient; it is based on cryptographic keys and signatures, so it is tamperproof; it does not rely on P2P techniques, and therefore it works.

The initial description of the idea can be found at https://fiatjaf.com/nostr.html. A less dry presentation of the idea can be found in [this video from Uncle Bob](https://www.youtube.com/watch?v=MaxXvcr181c).

## How it works

It's a very simple idea: each person can publish their notes to multiple relays (which are just simple servers), and people who follow them can connect to these relays and fetch the notes. The protocol just defines the messages that can be sent between clients and relays in order to publish and fetch the content they want.

![](diagram.jpg)

These relays can be hosted by anyone and have any rule or internal policy they want. The fact that the protocol is open makes it so that, as long as there is any relay willing to host someone, they can still publish their stuff for their followers, and the followers can find their stuff in that relay.

Relays can also lie about data published by others, but to ensure that isn't a problem, public-key cryptography is used and every note is signed. When you follow someone you're actually following their public key and clients will check notes received from relays to ensure they were properly signed. Here is a video that explains the role of relays pretty well: [nostr:nevent1qqsqhrasmmw0nnwjfeeka9sy4zl3c6rw5w2mtv4lugutl4luw57x7nqpr4mhxue69uhkummnw3ezucnfw33k76twv4ezuum0vd5kzmp0qyfhwumn8ghj7mmxve3ksctfdch8qatz9uq3wamnwvaz7tmjv4kxz7fwdehhxarj9e3xzmny9u76jrg5](https://njump.me/nevent1qqsqhrasmmw0nnwjfeeka9sy4zl3c6rw5w2mtv4lugutl4luw57x7nqpr4mhxue69uhkummnw3ezucnfw33k76twv4ezuum0vd5kzmp0qyfhwumn8ghj7mmxve3ksctfdch8qatz9uq3wamnwvaz7tmjv4kxz7fwdehhxarj9e3xzmny9u76jrg5).

The hardest part is how to find in which relay you will find notes of each person you follow, since they can be anywhere. There are multiple heuristics currently being used to approach this issue. An animated description of one possible flow can be seen at https://how-nostr-works.pages.dev/#/outbox.

## Protocol specification

See the [NIPs](https://github.com/nostr-protocol/nips) and especially [NIP-01](https://github.com/nostr-protocol/nips/blob/master/01.md) for a reasonably-detailed explanation of the protocol spec, it's very small.

## Getting started

There are many ways to get started using Nostr, but one simple and recommended way is to visit https://start.njump.me/ and go from there.

## Software

A list of mostly-ready to use apps is kept at https://nostrapps.com/.

A very big and daunting list of clients and libraries for all platforms and languages imaginable can be found at https://nostr.net/.

## License

Public domain.
