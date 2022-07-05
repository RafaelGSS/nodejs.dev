---
title: August 2021 Security Releases
blogAuthors: ['mhdawson']
category: 'vulnerabilities'
---

## _(Update 11-Aug-2021)_ Security releases available

Updates are now available for v16.x, v14.x, and v12.x Node.js release lines for the
following issues.

### cares upgrade - Improper handling of untypical characters in domain names (High) (CVE-2021-22931)

Node.js was vulnerable to Remote Code Execution, XSS, application crashes due to missing input
validation of host names returned by Domain Name Servers in the Node.js DNS library which can
lead to output of wrong hostnames (leading to Domain Hijacking) and injection vulnerabilities
in applications using the library.

You can read more about it in:
<https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-22931>

Impacts:

* All versions of the 16.x, 14.x, and 12.x releases lines

Thank you to Philipp Jeitner from Fraunhofer SIT for reporting this vulnerability.

### Use after free on close http2 on stream canceling (High) (CVE-2021-22940)

Node.js was vulnerable to a use after free attack where an attacker might be able to exploit
memory corruption to change process behavior. The issue is a follow on to CVE-2021-22930
as the issue was not completely resolved in the fix for CVE-2021-22930.

You can read more about it in:
<https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-22940>

Impacts:

* All versions of the 16.x, 14.x, and 12.x releases lines

Thank you to Eran Levin (exx8) for reporting the original vulnerability and those who helped identify the remaining issues.

### Incomplete validation of rejectUnauthorized parameter (Low) (CVE-2021-22939)

If the Node.js https API was used incorrectly and "undefined" was in passed for the
"rejectUnauthorized" parameter, no error was returned and connections
to servers with an expired certificate would have been accepted.

You can read more about it in:
<https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-22939>

Impacts:

* All versions of the 16.x, 14.x, and 12.x releases lines

Thank you to Tim Perry, from HTTP Toolkit for reporting this vulnerability.

## Downloads and release details

* [Node.js v12.22.5 (LTS)](https://nodejs.org/en/blog/release/v12.22.5/)
* [Node.js v14.17.5 (LTS)](https://nodejs.org/en/blog/release/v14.17.5/)
* [Node.js v16.6.2 (Current)](https://nodejs.org/en/blog/release/v16.6.2/)

***

# Summary

The Node.js project will release new versions of all supported release lines on or shortly after Wednesday
August 11th, 2021 in order to address:

* Two high severity issues and one low severity issue.

## Impact

The 16.x release line of Node.js is vulnerable to two high severity issues and one low severity issue.

The 14.x release line of Node.js is vulnerable to two high severity issues and one low severity issue.

The 12.x release line of Node.js is vulnerable to two high severity issues and one low severity issue.

## Release timing

Releases will be available at, or shortly after, Wednesday, August 11th, 2021.

## Contact and future updates

The current Node.js security policy can be found at <https://github.com/nodejs/node/blob/HEAD/SECURITY.md#security>. Please follow the process outlined in <https://github.com/nodejs/node/blob/master/SECURITY.md> if you wish to report a vulnerability in Node.js.

Subscribe to the low-volume announcement-only nodejs-sec mailing list at <https://groups.google.com/forum/#!forum/nodejs-sec> to stay up to date on security vulnerabilities and security-related releases of Node.js and the projects maintained in the nodejs GitHub organization.