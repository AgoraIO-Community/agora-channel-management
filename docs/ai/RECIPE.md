# Channel Management Sample

## Overview

Inspect channel users and manage user-privilege rules with the browser-based Agora REST API tester.

Repository: [AgoraIO-Community/agora-channel-management](https://github.com/AgoraIO-Community/agora-channel-management)

## Prerequisites and Setup

1. Serve the repository's `index.html` with a local static HTTP server and open it in a browser. There is no package install or build step in this repository.
2. Open Set API Credentials and enter a test project's App ID, Customer ID and Customer Secret.
3. Use Query Channel Users first to inspect a test channel. To exercise rule management, use a disposable test user and channel; enter the UID, expiration and privilege, then create, query, update and delete the rule.

## What To Check

- Check the displayed JSON response and browser network errors for each request.
- Verify that the test rule affects only the intended UID and is deleted after testing.

## Integration Notes

This is a REST API tester, not an RTC publishing client. It sends credentials directly from the browser and persists them in localStorage. Keep testing isolated, clear stored credentials afterward, and move privileged calls behind an authenticated backend for production. The referenced `modern-ui-library.css` is absent from this repository, so styling may be incomplete.

Keep App Certificates, customer secrets and privileged token generation on a trusted backend for production. Use only your own test credentials while configuring historical demos; do not commit them. Preserve the sample's existing dependency versions and lifecycle until a separate migration is tested.

## Source References

- [README.md](../../README.md)
- [index.html](../../index.html)

## Validation Status

This recipe was checked against the repository's source and setup documents. The platform build and live service/device flow have not been run as part of this documentation change. Complete the checks above in an environment with the required SDKs, hardware and service access before treating it as a validated deployment.

## Implementation Prompt

```text
You are working in AgoraIO-Community/agora-channel-management. Use docs/ai/RECIPE.md and its linked source files to adapt the Channel Management Sample reference to this project.

Start by inspecting the actual sample directory and configuration described above. Resolve its listed missing prerequisites before claiming it is runnable. Preserve the existing architecture and compatible dependency versions. Implement the recipe's feature-specific flow, permissions and resource cleanup. Use a trusted backend for privileged credentials and tokens in production.

Run the repository-specific build or launch flow, then perform each What To Check item. Report the commands run, the observed results and anything blocked by service access, hardware or incomplete sample code. Do not claim live validation from a documentation or catalog build alone.
```
