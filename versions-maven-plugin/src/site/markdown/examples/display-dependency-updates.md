title: Checking for new dependency updates
author: Stephen Connolly
date: 2008-09-02

<!---
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at
  https://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

# Checking for new dependency updates

The `display-dependency-updates` goal will check all the dependencies used in your project and display a list
of those dependencies with newer versions available.

Here are some examples of what this looks like:

```sh
svn checkout http://svn.codehaus.org/mojo/trunk/mojo/build-helper-maven-plugin build-helper-maven-plugin
cd build-helper-maven-plugin
mvn versions:display-dependency-updates
```

Which produces the following output:

```sh
[INFO] ------------------------------------------------------------------------
[INFO] Building Build Helper Maven Plugin
[INFO]    task-segment: [versions:display-dependency-updates]
[INFO] ------------------------------------------------------------------------
[INFO] [versions:display-dependency-updates]
[INFO]
[INFO] The following dependency updates are available:
[INFO]   org.apache.maven:maven-artifact ........................ 2.0 -> 2.0.9
[INFO]   org.apache.maven:maven-plugin-api ...................... 2.0 -> 2.0.9
[INFO]   org.apache.maven:maven-project ....................... 2.0.2 -> 2.0.9
[INFO]   org.codehaus.plexus:plexus-utils ....................... 1.1 -> 1.5.6
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESSFUL
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 17 seconds
[INFO] Finished at: Fri Aug 15 10:46:03 IST 2008
[INFO] Final Memory: 10M/167M
[INFO] ------------------------------------------------------------------------
```
