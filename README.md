# Subscription management

Your task is to create a server that exposes an API to manage subscriptions, creating, checking their status etc.

## Description

Your server should expose an API via either [`REST`](https://en.wikipedia.org/wiki/Representational_state_transfer)
or [`graphql`](https://graphql.org/).

The API should support:

* creating a new subscription for a `msisdn` with an `activate_at` date and a type;
    * if a non-cancelled subscription already has the same `msisdn` the request should be rejected;
* fetching information about a subscription, which should show:
    * all of the subscription's data,
    * as well as which operator owns the subscription (using the API provided
      by [`PTS`](https://catalog.pts.se/);
* changing the activation date of a pending subscription;
* pausing and reactivating the subscription;
* cancelling the subscription.

### The subscription data model

A subscription represents a user's phone subscription, which has the following information:

* [`msisdn`](https://en.wikipedia.org/wiki/MSISDN) which is the subscription's number;
* `activate_at` which is the date when the subscription is activated in the system;
* `type` which is either [`PBX`](https://en.wikipedia.org/wiki/Business_telephone_system#Private_branch_exchange)
  or [`CELL`](https://en.wikipedia.org/wiki/Mobile_phone);
* `status` which is one of `pending`, `activated`, `paused` or `cancelled`.

## Submission

You should submit your code by using [`git bundle`](https://git-scm.com/docs/git-bundle.html) and sending the bundled
file via mail.

_* Your work will not be used in the Telness product or in any part of such product, the only purpose is to test your
technical skills._

## Requirements

* Your submission should include a `README.md` file documenting how to install start and test the project;
* You won't have the time to make everything perfect, just document what is lacking and how you would improve it;
* Do not make the task harder than it is, it should take a couple of hours but absolutely not more than 8 hours;
* You are free to use any technology and framework of your choice.
