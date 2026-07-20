# Quick Generate Link with Linkila

Creates a new link and short URL in Linkila.

## Endpoint

- **Method:** `POST`
- **Path:** `/quickGenerate`
- **Base URL:** `https://app.linkila.com/integrations/api/v1`
- **Official documentation:** [Quick Generate Link](https://app.linkila.com/integrations/api/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetURL` | body | `string` | no | Required destination URL for the new Linkila short link. |
| `domainName` | body | `string` | no | Optional Linkila domain name for the generated short link. |
| `slug` | body | `string` | no | Optional custom slug for the generated short link. |
| `title` | body | `string` | no | Optional title for the generated short link. |
| `deepLinkEnabled` | body | `boolean` | no | Whether deep-link behavior should be enabled for the generated link. |
