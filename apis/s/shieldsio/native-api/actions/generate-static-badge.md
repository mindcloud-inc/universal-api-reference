# Generate Static Badge with Shields.io

Retrieves a custom static badge image from Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/:badgeContent`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Static Badge](https://shields.io/badges/static-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badgeContent` | path | `string` | yes | Path content for the badge, encoded as label-message-color or message-color separated by dashes. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
| `logo` | query | `string` | no | Simple Icons slug for an optional badge logo. |
| `label` | query | `string` | no | Override the badge left-side label text. |
