# DethemeKit for Elementor - Security Patched

This repository contains a security-patched version of the DethemeKit for Elementor WordPress plugin.

## Security Fix

**Vulnerability Fixed:** Broken Access Control in WordPress DethemeKit For Elementor Plugin <= 2.1.10

This patched version (2.1.10.5) fixes a Broken Access Control vulnerability by implementing proper security checks in the template manager AJAX handlers:

1. Added proper capability checks with `current_user_can('edit_posts')` to ensure only users with appropriate permissions can access sensitive functionality
2. Added nonce verification with `wp_verify_nonce()` to protect against CSRF attacks

## Changes Made

1. Fixed the `get_template_data` method in `includes/templates/classes/manager.php` by implementing proper security checks
2. Updated plugin version to 2.1.10.5
3. Renamed plugin to "DethemeKit for Elementor Patched" to distinguish it from the original

## Vulnerability Details

- CVSS Score: 5.3
- Vulnerability Type: Broken Access Control
- Affected Versions: <= 2.1.10
- Fixed Version: 2.1.10.5 (this patched version)

## Installation

1. Download the ZIP file from this repository
2. In your WordPress admin, go to Plugins > Add New > Upload Plugin
3. Upload the ZIP file and activate the plugin

## Credits

This security patch was created on June 14, 2025.

Original plugin by deTheme: https://detheme.com