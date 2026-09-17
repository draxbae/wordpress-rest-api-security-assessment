# WordPress REST API Security Assessment

Security assessment of the WordPress REST API Batch Requests feature, including vulnerability reproduction, version comparison, patch validation, and post-patch retesting in a controlled lab environment.

## Overview

This project documents a controlled security assessment of the WordPress REST API Batch Requests functionality.

The assessment focused on understanding the behavior of the Batch API, reproducing the issue in a controlled environment, applying the vendor patch by upgrading WordPress, and performing a post-patch retest.

## Environment

- **Application:** WordPress
- **Initial Version:** 7.0.0
- **Patched Version:** 7.0.2
- **Environment:** Docker
- **PHP:** 8.3
- **Component:** WordPress REST API
- **Feature:** Batch Requests
- **Endpoint:** `/batch/v1`

## Assessment Flow

The assessment was performed using the following workflow:

1. Deploy WordPress 7.0.0 in a controlled lab environment.
2. Identify the REST API Batch Requests implementation.
3. Review the relevant server-side request handling logic.
4. Reproduce the observed behavior through the Batch API endpoint.
5. Upgrade WordPress from 7.0.0 to 7.0.2.
6. Repeat the same test after the patch.
7. Compare the behavior before and after the update.

## Technical Area

The relevant implementation is located in:

```text
wp-includes/rest-api/class-wp-rest-server.php
