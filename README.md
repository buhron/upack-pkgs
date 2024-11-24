If you want to request to add a package, feel free to make a PR
* Add extracted path (required) at `/packages/<packagename>/extracted/`
* Add zipped file (this is optional) at `/packages/<packagename>/zipped/<zip file>`
* Config file (required) at `/packages/<packagename/crospack-config/<version>-pkgconfig`
* 8Gb Max
* Shouldn't interfere with the system (for example, a script modifiying the UEFI firmware, if you want to publish a system-need package, feel free to do it at the crospack-uncheckedpkgs repo)
