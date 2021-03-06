Inventit IoT Developer Network (IIDN) Command Line Interface Tool
===
iidn-cli is a command line tool offering you to interact with IIDN sandbox.

## What iidn-cli offers
The tool enables you:

* to sign up to IIDN sandbox with your OAuth2 account such as [Facebook](http://www.facebook.com/) and [GitHub](https://github.com)
 * Use <code>reset</code> command when you forget your API credentials (<code>app_id</code>, <code>client_id</code> and <code>client_secret</code>)
* to reset your API secret (<code>client_secret</code>) with your OAuth2 account
* to upload your [MOAT js](http://dev.yourinventit.com/references/moat-js-api-document) server side applications to the sandbox
* to upload your [MOAT Java](http://dev.yourinventit.com/references/moat-java-api-document) and/or MOAT C applications to the sandbox
* to tail a [MOAT js](http://dev.yourinventit.com/references/moat-js-api-document) server side application log
* to download a secure token for you to sign it with your application certificate private key and embed it to your application
  (The gateway application uses the signed secure token for verification as well.)
* to download system managed binaries

## Authentication Arguments

As of 1.0.1-r4, iidn-cli accepts credentials as command line arguments.

    sh ./iidn <command> <command_params> --app_id=YOUR_APP_ID \
        --client_id=YOUR_CLIENT_ID --client_secret=YOUR_CLIENT_SECRET

## Prerequisites
The tool requires one of the following runtimes:

* Node.js, v0.8.8+, or
* Sun/Oracle/Apple JDK, 1.6+ (Not a JRE. OpenJDK may work though not confirmed.)

## Installation

Check out the source code with the git command.

	mkdir -p path/to/iidn
	cd path/to/iidn
	git clone git:git@github.com:inventit/iidn-cli.git

Then run the following command:

	sh ./iidn [COMMAND HERE]

## Get Started

See [the tutorial](http://dev.yourinventit.com/guides/get-started) to learn more.

## Source Code License

All program source codes are available under the MIT style License.

The use of IIDN service requires [our term of service](http://dev.yourinventit.com/legal/term-of-service).

Copyright (c) 2013 Inventit Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Change History

1.0.1-r4 : February 15, 2013  

* `iidn` command now takes credentials as arguments

1.0.1-r3 : February 13, 2013  

* `iidn` command without arguments may not work on some environment
* Fixes an issue where a browser opening function aborts the process when the terminal doesn't working on any display system
* Changes the shell type declaration in `iidn`, explicitly referring to `bash`

1.0.1-r2 : February 8, 2013  

* Fixes issues where sydownload always overwrites a local file with the latest downloaded chunk

1.0.1-r1 : February 7, 2013  

* Fixes issues where jsdeploy doesn't work on Rhino runtime

1.0.1 : January 31, 2013  

* Adds a new command to reset an API secret
* Changes the version number to synchronize with MOAT REST API version

0.2.5 : January 16, 2013  

* Fixes an issue where a large EULA text isn't displayed properly

0.2.4 : January 16, 2013  

* Fixes an issue where a large ToS text isn't displayed properly

0.2.3 : January 13, 2013  

* Fixes an issue where Rhino script fails to set the content type

0.2.2 : January 9, 2013  

* Fixes an issue where binary download command (sysdownload) generates corrupted content file because of failure of handling chunked binary data

0.2.1 : January 9, 2013  

* Updates the copyright year

0.2.0 : January 9, 2013  

* Changing deploy/undeploy commands to deployjs/undeployjs
* Adds new commands, deploybin/undeploybin for deploying/undeploying arbitrary distribution application packages for devices/gateways
* Adds a new command 'sysdownload' allowing users to download packages managed by the sandbox server

0.1.0 : December 10, 2012

* Initial Release.
