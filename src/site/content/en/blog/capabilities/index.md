---
title: Unlocking New Capabilities for the Web
subhead: We strongly believe that every developer should have access to the capabilities they need to make a great web experience, and we are committed to a more capable web. Learn about some of the new APIs we're considering and how you can get involved.
authors:
  - petelepage
  - thomassteiner
date: 2019-05-23
hero: capabilities-process.jpg
alt: The capabilities process consisting of identifying the need, writing the explainer, soliciting feedback, writing a formal spec, and shipping it.
description: |
  Web apps should be able to do anything native apps can. Through Project Fugu, we want to make it
  possible to build and deliver any kind of app on the open web.
tags:
  - post
  - capabilities
---

{% Aside 'success' %}
  Web apps should be able to do anything native apps can.
  We want to make it possible for you to build and deliver apps on the open
  web that have never been possible before.
{% endAside %}

<div class="video-wrapper">
  <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/GSiUzuB-PoI"
          frameborder="0"
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
          style="position:relative"
  ></iframe>
</div>

The web is an amazing platform, it reaches users all around the world - on
essentially any device. It’s easy to use, and easy to share. There’s nothing
to install. But most importantly, it’s an open-ecosystem that anyone can use
or build on.

There are some apps that are not possible to build and deliver on the open
web today. We call this, the *app gap*. The gap between what’s possible on the
web and what’s possible on native. We want to close that gap. We believe web
apps should be able to do anything native apps can.

> Through our capabilities project, we want to make it possible for web apps
> to do anything native apps can, by exposing the capabilities of native
> platforms to the web platform, while maintaining user security, privacy,
> trust, and other core tenets of the web.

## The new capabilities

You can see the [full list](crbug.com/?q=proj-fugu) of capabilities we're
considering on [crbug.com](https://crbug.com) and filtering issues with the
`proj-fugu` label.

{% Aside %}
  **Have a suggestion for a capability you think we should consider?**
  Tell us about it by filing a [new feature
  request](https://goo.gl/qWhHXU). Please be sure to include as much detail as you can, such as
  the problem you're trying to solve, suggested use cases, and anything else
  that might be helpful.
{% endAside %}

### Capabilities in flight

<table>
  <thead>
    <tr>
      <th>Capability</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="/web/updates/2018/12/badging-api">Badging API</a>
      </td>
      <td>
        The Badging API is a new web platform API that allows installed web
        apps to set an application-wide badge, shown in an
        operating-system-specific place associated with the application, such
        as the shelf or home screen. Badging makes it easy to subtly notify
        the user that there is some new activity that might require their
        attention, or it can be used to indicate a small amount of information,
        such as an unread count.
        <br><br>
        <b>Current Status:</b> Available as an origin trial.<br>
        <b>Last Updated:</b> March 12th, 2019
      </td>
    </tr>
    <tr>
      <td>
        <a href="/web/updates/2018/12/get-installed-related-apps">
          Get Installed Related Apps API
        </a>
      </td>
      <td>
        The <code>getInstalledRelatedApps</code> API is a new web platform API
        that allows your web app to check to see if your native app is
        installed on the users device, and vice versa.
        <br><br>
        <b>Current Status:</b> Available as an origin trial.<br>
        <b>Last Updated:</b> March 12th, 2019
      </td>
    </tr>
    <tr>
      <td>
        <a href="/web/updates/2019/01/shape-detection">Shape Detection API</a>
      </td>
      <td>
        The Shape Detection API opens up native implementations of shape
        detection services and exposes them through a set of JavaScript
        interfaces. Currently, the supported features are face detection,
        barcode detection, and text detection (Optical Character Recognition).
        <br><br>
        <b>Current Status:</b> Available as an origin trial.<br>
        <b>Last Updated:</b> February 2nd, 2019
      </td>
    <tr>
      <td>
        <a href="/web/updates/2018/12/wakelock">Wake Lock API</a>
      </td>
      <td>
        To avoid draining the battery, most devices will quickly fall asleep
        when left idle. While this is fine for most of the time, there are
        some applications that need to keep the screen or the device awake in
        order to complete some work. The Wake Lock API provides a way to
        prevent the device from dimming or locking the screen or prevent
        the device from going to sleep when an application needs to keep
        running.
        <br><br>
        <b>Current Status:</b> Gathering feedback &amp; iterating on design.<br>
        <b>Last Updated:</b> December 18th, 2018
      </td>
    </tr>
    <tr>
      <td>
        <a href="/web/updates/2018/11/writable-files">Writable Files API</a>
      </td>
      <td>
        The writable files API is designed to increase interoperability of
        web applications with native applications, making it possible for users
        to choose files or directories that a web app can interact with on the
        native file system, and without having to use a native wrapper like
        Electron to ship your web app.
        <br><br>
        <b>Current Status:</b> Gathering feedback &amp; iterating on design.<br>
        <b>Last Updated:</b> November 12th, 2018
      </td>
    </tr>
  </tbody>
</table>

### Launched capabilities

<table>
  <thead>
    <tr>
      <th>Capability</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="/web/updates/2018/12/web-share-target">Web Share Target</a>
      </td>
      <td>
        The Web Share Target API allows installed web apps to register with
        the underlying OS as a share target to receive shared content from
        either the Web Share API or system events, like the OS-level share
        button.
        <br><br>
        <b>Status:</b> Launched in Chrome 71<br>
        <b>Last Updated:</b> December 5th, 2018
      </td>
    </tr>
  </tbody>
</table>

{% Aside 'codelab' %}
  **Want to try some of these new capabilities?** Check out the
  [Web Capabilities Codelab](https://codelabs.developers.google.com/codelabs/web-capabilities/)
{% endAside %}

## How will we design & implement these new capabilities?

<img src="capabilities-process.jpg">

We developed this process to make it possible to design and develop new web
platform capabilities that meet the needs of developers quickly, in the open,
and most importantly, work within the existing standards process. It’s no
different than how we develop every other web platform feature, but it puts an
emphasis on developer feedback.

Developer feedback is critical to help us ensure we’re shipping the right
features, but when it comes in late in the process, it can be hard to change
course. That’s why we’re starting to ask for feedback earlier. When actionable
technical and use-case feedback comes in early, it’s easier to course correct or
even stop development, without having shipped poorly thought out or badly
implemented features. Features being developed at WICG are not set in stone, and
[your input](https://discourse.wicg.io/) can make a big difference in how they
evolve.

It’s worth noting that many ideas never make it past the explainer or [origin
trial](https://github.com/GoogleChrome/OriginTrials/blob/gh-pages/developer-guide.md)
stage. The goal of the process is to ship the right feature. That
means we need to learn and iterate quickly. Not shipping a feature because it
doesn’t solve the developer need is OK. To enable this learning, we have come to
employ the following process—although there is frequently some re-ordering of
later steps due to feedback:

### Identify the developer need

The first step is to identify and understand the developer need. What is the
developer trying to accomplish? Who would use it? How are they doing it today?
And what problems or frustrations are fixed by this new capability. Typically,
these come in as feature request from developers, frequently through [bugs filed
on bugs.chromium.org](https://bugs.chromium.org/p/chromium/issues/list?can=2&q=Type%3DFeature).

### Create an explainer

After identifying the need for a new capability, create an
[explainer](https://github.com/w3ctag/w3ctag.github.io/blob/master/explainers.md),
essentially a design doc that is meant to explain the problem, along with some
sample code showing how the API might work. The explainer is a living design
document that will go through heavy iteration as the new capability evolves.

### Get feedback and iterate on the explainer

Once the explainer has a reasonable level of clarity, it’s time to publicize it,
to solicit feedback, and iterate on the design. This is an opportunity to verify
the new capability meets the needs of developers and works in a way that they
expect. This is also an opportunity to gather public support and verify that
there really is a need for this capability.

### Move the design to a specification & iterate

Once the explainer is in a good state, the design work transitions into a
formal specification, working with developers and other browser vendors to
iterate and improve on the design.

Then, once the design starts to stabilize, we typically use an
[origin trial](https://github.com/GoogleChrome/OriginTrials) to experiment
with the implementation. Origin trials allow you to try new features with
real users, and give feedback on the implementation. This real world feedback
helps shape and validate the design, ensuring we get it right, before it
becomes a standard.

### Ship it

Finally, once the origin trial is complete, the spec has been finalized, and
all of the other launch steps have been completed, it’s time to ship it to
stable.

## Design for user security, privacy, and trust

Some of these features may seem scary at first, especially in light of how
they’re implemented on native. But the web is inherently safer than native,
opening a web page shouldn’t be scary.

Nothing should ever be granted access by default, but instead rely on a
permission model that puts the user in total control, and is easily
revoke-able. It needs to be crystal clear when, and how these APIs are being
used. We've outlined some of our thought process in
[Controlling Access to Powerful Web Platform Features](https://bit.ly/powerful-apis).