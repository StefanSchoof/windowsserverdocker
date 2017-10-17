# windowsserverdocker

This is a workaround to trigger a build in VSTS. See https://stackoverflow.com/questions/46681620.

This repro is configured as Automated Build with a Linked Repositories to [microsoft/windowsservercore](https://hub.docker.com/r/microsoft/windowsservercore/). It builds the [alpine](https://hub.docker.com/_/alpine/) image because the automated build host currently does not build windows. On Image Push is a webhook configured. This webhook starts a [MS Flow](https://flow.microsoft.com) with http trigger and with a VSTS Build Action.