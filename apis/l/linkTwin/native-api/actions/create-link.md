# Create Link with LinkTwin

Creates a new shortened link in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/url/add`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Create Link](https://linktw.in/developers#create-a-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Long URL to shorten. |
| `custom` | body | `string` | no | Custom alias instead of a random alias. |
| `password` | body | `string` | no | Password protection for the link. |
| `domain` | body | `string` | no | Branded domain that already exists in the account. |
| `expiry` | body | `string` | no | Expiration date and time for the link. |
| `clicklimit` | body | `number` | no | Maximum number of clicks before the link expires. |
| `expirationredirect` | body | `string` | no | Redirect URL after expiration. |
| `note` | body | `string` | no | Internal note for the link. |
| `display_title` | body | `string` | no | Dashboard-only title for the link. |
| `geotarget` | body | `object<object>` | no | Geo targeting rules. Send multiple values as a array. |
| `devicetarget` | body | `object<object>` | no | Device targeting rules. Send multiple values as a array. |
| `languagetarget` | body | `object<object>` | no | Language targeting rules. Send multiple values as a array. |
| `abtesting` | body | `object<object>` | no | A/B testing variants. Send multiple values as a array. |
| `parameters` | body | `object<object>` | no | URL parameters to append. Send multiple values as a array. |
| `metatitle` | body | `string` | no | Meta title. |
| `metadescription` | body | `string` | no | Meta description. |
| `metaimage` | body | `string` | no | Social share preview image URL. |
| `pixels` | body | `string` | no | Pixel IDs or names to attach. Send multiple values as a array. |
| `collections` | body | `string` | no | Collection IDs or names to add the link to. Send multiple values as a array. |
