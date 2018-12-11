# Contributing & DevCall

Contact information for the core dev team. Developers are also most welcome to attend the [weekly dev call](./#dev_call) and other [developer events](./#calendar).

## Support

### Weekly Dev Call <a id="dev_call"></a>

The SDK core dev team syncs up on platform technical details and in-depth analysis. There is also space in the agenda to discuss pull requests, major impacting issues and Q&A.

#### Who should attend:

* Core project maintainers
* Component maintainers
* Test team lead

> **Tip** The dev call is open to all interested developers \(not just the core dev team\). This is a great opportunity to meet the team and contribute to the ongoing development of the platform.

#### Schedule

* TIME: Tuesday 3PM UTC+8, X CET, X EST, X PST \([subscribe to calendar](https://calendar.google.com/calendar/ical/px4.io_fs35jm7ugmvahv5juhhr3tkkf0%40group.calendar.google.com/public/basic.ics)\)
* **Join the call**: Skype link\(need to add\)
* Agenda is published before the call on [Develop Discuss - weekly-dev-call](http:)

### Calendar & Events <a id="calendar"></a>

The _SDK Core Team Calendar_ shows important events for platform developers and users. Select the links below to display the calendar in your timezone \(and to add it to your own calendar\):

**Note:** calendar defaults to CET.

## Contribution

### Code of Conduct

We pledge to adhere to the [SDK code of conduct](https://confluence.sw.nxp.com/display/MCUXSDK/MCUXpresso+SDK+Coding+Style+and+Naming+Convention>). This code aims to foster an open and welcoming environment for inner NXP developers.

### Source Code Management

The SDK project uses a three-branch Git branching model:

* [master](./) is by default unstable and sees rapid development.
* [beta](https://github.com/Summercore/NXP_DEV_GUIDE/tree/150ec95ff004d5c2b1dc522643b97470763fa5b1/contribute/rc/README.md) has been thoroughly tested. It's intended for testers.
* [stable](https://github.com/Summercore/NXP_DEV_GUIDE/tree/150ec95ff004d5c2b1dc522643b97470763fa5b1/contribute/rfp/README.md) points to the last release.

We try to retain a [linear history through rebases](https://www.atlassian.com/git/tutorials/rewriting-history) and avoid the [Github flow](https://guides.github.com/introduction/flow/). However, due to the global team and fast moving development we might resort to merges at times.

To contribute new functionality, [sign up for bitbucket](https://bitbucket.sw.nxp.com/projects/MCUCORE/repos/mcu-sdk-2.0/browse), then [fork/clone](ssh://git@bitbucket.sw.nxp.com/mcucore/mcu-sdk-2.0.git) the repository, create a new branch, add your changes, and finally [send a pull request](https://help.github.com/articles/using-pull-requests/). Changes will be merged when they pass our [continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) tests.

All code contributions have to be under the permissive [BSD 3-clause license](https://opensource.org/licenses/BSD-3-Clause) and all code must not impose any further constraints on the use.

### Commits and Commit Messages

Please use descriptive, multi-paragraph commit messages for all non-trivial changes. Structure them well so they make sense in the one-line summary but also provide full detail.

```text
Component: Explain the change in one sentence. Fixes #1234

Prepend the software component to the start of the summary
line, either by the module name or a description of it.
    (e.g. "I2C" or "i2c_polling_b2b_transfer").

If the issue number is appended as <Fixes #1234>, Github
will automatically close the issue when the commit is
merged to the master branch.

The body of the message can contain several paragraphs.
Describe in detail what you changed. Link issues either
related to this fix or to the testing results of this
commit.

Describe the change and why you changed it, avoid to
paraphrase the code change (Good: "Adds an additional
bus NACK status flag for i2c bus with no slave ack".
Bad: "status_NACK").

Reported-by: Name <email@nxp.com>
```

**Use** `git commit -s` **to sign off on all of your commits.** This will add `signed-off-by:` with your name and email as the last line.

This commit guide is based on best practices for the Linux Kernel and other [projects maintained](https://github.com/torvalds/subsurface/blob/a48494d2fbed58c751e9b7e8fbff88582f9b2d02/README#L88-L115) by Linus Torvalds.

