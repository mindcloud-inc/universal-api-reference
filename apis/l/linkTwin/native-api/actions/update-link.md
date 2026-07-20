# Update Link with LinkTwin

Updates an existing link in LinkTwin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/url/:id/update`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Update Link](https://linktw.in/developers#update-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Link ID. |
| `url` | body | `string` | no | Long URL to update to. |
| `custom` | body | `string` | no | Custom alias. |
| `password` | body | `string` | no | Password protection. Send null to remove. |
| `domain` | body | `string` | no | Branded domain that already exists in the account. |
| `expiry` | body | `string` | no | Expiration date and time. Send null to remove. |
| `clicklimit` | body | `number` | no | Maximum number of clicks before the link expires. Send null to remove. |
| `expirationredirect` | body | `string` | no | Redirect URL after expiration. Send null to remove. |
| `note` | body | `string` | no | Internal note. Send null to remove. |
| `display_title` | body | `string` | no | Dashboard-only title. Send null to remove. |
| `geotarget` | body | `object<object>` | no | Geo targeting rules. Send [] to clear all. Send multiple values as a array. |
| `devicetarget` | body | `object<object>` | no | Device targeting rules. Send [] to clear all. Send multiple values as a array. |
| `languagetarget` | body | `object<object>` | no | Language targeting rules. Send [] to clear all. Send multiple values as a array. |
| `abtesting` | body | `object<object>` | no | A/B testing variants. Send [] to clear all. Send multiple values as a array. |
| `parameters` | body | `object<object>` | no | URL parameters. Send [] to clear all. Send multiple values as a array. |
| `metatitle` | body | `string` | no | Meta title. Send null to remove. |
| `metadescription` | body | `string` | no | Meta description. Send null to remove. |
| `metaimage` | body | `string` | no | Social share preview image URL. Send null to remove. |
| `pixels` | body | `string` | no | Pixel IDs or names. Send [] to remove all. Send multiple values as a array. |
| `collections` | body | `string` | no | Collection IDs or names. Send [] to remove from all collections. Send multiple values as a array. |
