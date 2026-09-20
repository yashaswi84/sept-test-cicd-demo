# CICD-Demo

[![Scanned by Frogbot](https://raw.github.com/jfrog/frogbot/master/images/frogbot-badge.svg)](https://docs.jfrog-applications.jfrog.io/jfrog-applications/frogbot)

## Overview

This is a demo how to integrate JFrog Artifactory with GitHub. 

Today we showcase

- OICD integration - seemless integration of the JFrog plattform with GitHub actions.
- Show results of security scans in the GitHub's build summaries.
- Block malicious packages with JFrog Curation.

#### - Showcase maliscious package detection, please add this line

Usually there is already a brach named "malicious". If this branch is missing, create a new branch and add

`    "cors.js": "0.0.1-security",`

in the "dependencies" section of the `package.json`file.

Try a GitHub Actions build afterwards for this branch. The build should fail and the build summary should explain, that a policy violation is causing the failure.
