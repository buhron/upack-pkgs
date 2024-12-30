If you want to request to add a package, feel free to make a PR <br />
* Add zipped file (required) at `/packages/<packagename>/zipped/<zip file>`
* Config file (required, JSON format) at `<zipped package>/upack.cfg`
* 4 GB max for zipped archive
* Packages that attack the system (viruses) or hardware will not be accepted.
  * If you want to publish an package not fitting this requirement, feel free to do at the upack-unverified-pkgs repo on my account
### Example config file
An example of an config file of a package named `zapzip` would look like:
```json
{
 "name": "zapzip", # i shouldn't point this out, as its pretty obvious
 "desc": "A fake package used for an example config file for an package manager", # description of package. the description is not used by upack, but used for browsing packages.
 "depends": [], # put dependencies here. upack will automatically install them
 "configuration_command": "zapzip init", # any shell command that configures the package for use. upack will automatically run this command once package is installed.
 "recommends": [], # recommended packages for zapzip (our example package) to work properly, or to maybe give more features to zipzap. upack will point out the recommended packages on pre-install.
 "req_root": false, # whether the package requires root or not. some packages may need root to add system users or maybe... idk
 "removal_command": "rm -rf ~/.local/share/zapzip ~/.zapzip" # any shell command that is run when specific package is removed. upack will automatically run this command once package is removed.
}
```
