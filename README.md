# netmatch.me

> [!NOTE]
> Tired of swiping through endless profiles that tell you nothing?
> netmatch.me is a new kind of connection app that matche
>  you with people based on what you **love**, not just how you look.
>
> In a privacy-first manner.

## Why?

Inspired by [a video of the channel "Not
Dave"](https://www.youtube.com/watch?v=o879xRxmwmU), in which he explain on
network theory and shows who is audience by analysis the channels they are
subscribed to. It's a great watch and absolutelly worth your time.

After instantly subscribing to the channel, I was impressed with accuracy in
which his audience interests matches mine, I commented:

> This is spot on! I wonder why no one built a dating app based on YouTube
> subscriptions... a bunch of seemly cool people, yet... Wait, I'm a developer.
>
> I'll tackle this in the coming weeks and post as a reply to this comment.

That comment received over 200 likes and 30 replies in just 6 days! This
overwhelming response validated there is clear a need for a different kind of
connection platform, thus deserved a serious project.

> [!NOTE]
> We are surrounded by like-minded people. What if we could actually connect
them?

## The Big Idea: Your Connections are Hiding in Plain Sight

Here’s the thing about communities: you’re already in them. Your Discord
server, your local church, your university. These
are spaces built on shared interests and, most importantly, **trust**.

But they are also full of missed connections.

That lifelong friend or partner could be right there, craving the same
connection you are. It might be the person in your guild who only posts memes,
so you never strike up a real conversation. Or the regular at your local
community event who seems quiet, so you assume they’re just part of "the boring
bunch."

You have more in common with these people than with 99% of the profiles on a
swipe-based app. But you'll never know because you’re separated by the sheer
number of faces or the fear of making an unsolicited advance. They remain just
another username in a sea of thousands.

`netmatch.me` is designed to bridge that gap. It uncovers the hidden network of
shared passions that already exists around you by looking not just at YouTube,
but at Spotify, Netflix, Goodreads, and more. It connects the dots between your
actual interests and the people you already trust.

## How It Works: Anonymous Matchmaking on a Trusted Instance

Your privacy isn't just a feature; it's the core of our design. The central
challenge is: "How can we find someone with similar taste without ever seeing
what you actually like?"

- **Trust Your Instance:** You connect your accounts (YouTube, Spotify, etc.) to
a netmatch.me instance you trust. This could be the official one, one hosted by
your community, or one you host yourself. Your data lives on this instance and
this instance alone.

- **Generate a "Taste Fingerprint":** Here’s where the magic happens. Your
instance analyzes your interests: the artists, shows, and games you love and
converts them into a privacy-preserving "Taste Fingerprint." (maybe embeddings
with Locality-Sensitive Hashing?). 
This is an abstract, anonymized representation of your unique profile.
Crucially, this fingerprint understands similarity. It knows that two different
sci-fi movies are related, or that two indie rock bands share a similar sound,
without ever exposing the specific titles to anyone, not even us.
  > Developing and refining this is our primary goal right now.

- **Match Anonymously:** Your instance communicates with other federated
instances using only these anonymous fingerprints. It can find a
high-compatibility match based on taste similarity without ever revealing the
underlying data.

- **Consent is Key:** Only when a mutual match is found does the process of
revealing more information begin. The app will ask both parties for consent to
share limited details (like a chosen display name or a few common interests).
Photos and real names are only shared after another explicit layer of consent
from both users.

The result: **Better matches, zero surveillance, and you control where your
data lives.**

## The Federated Approach

This isn't just about technical architecture: it's about putting power back into
the hands of communities. By using the same federated principles as Mastodon or
[the ForgeFed initiative](https://forgefed.org/), we aim enable true social
sovereignty.

Each community can spin up an instance and decide its own rules:
-   Stay completely private.
-   Federate with a few trusted communities.
-   Connect to the main network for maximum reach.

You trust your community admins. You don't have to trust us.

## An Open Protocol: A Call for Collaboration

The technical details of the federation protocol are a work in progress. We are
actively discussing the best way to implement this vision by leveraging the
existing infrastructure of the Fediverse.

This is a proposal, and we need the community's help to iron out the
nitty-gritty details. Our hope is that this standard could one day be adopted
by larger platforms. Imagine finding a match directly from your Mastodon
instance. That's the future we're building towards.

## Roadmap

-   **July 2025:** Live website and Fediverse [protocol draft](https://github.com/Netmatch-me/protocol).
-   **September 2025:** PWA and web app beta.
-   **December 2025:** Native iOS and Android apps.
-   **February 2026:** Open-source launch and federation support.

> Yeah, it's ambitious! But after a decade building apps and leading dev teams,
> I'm confident we'll get there, even if we have to nudge the timeline a bit.

## Tech Stack

-   **Backend:** Go
-   **Database:** SQLite / PostgreSQL
-   **Web & PWA:** SvelteKit
-   **Mobile:** React Native

## Contributing

Want to help? If you have experience with the **Fediverse**, **ActivityPub**,
or any part of our **tech stack**, we need you! The protocol will be developed
in the open from day one.

If you'd like to support the project financially, you can sponsor me (@nathabonfim59).

Right now, the dev team is small for focus, but if you're passionate and have
the right skills, reach out: **dev@netmatch.me**.

## Join the Beta

Want early access? **[Sign up for the beta on our
website!](https://netmatch.me)** (Just your name and email. We pledge to never
sell your data.)
