# Update Link with JmpTo

Updates an existing link in JmpTo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/url/:id/update`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Update Link](https://jmpto.net/developers#update-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | body | `string` | no | Campaign ID. |
| `channel` | body | `string` | no | Channel ID. |
| `custom` | body | `string` | no | Custom alias instead of a random alias. |
| `domain` | body | `string` | no | Custom domain for the link. |
| `expiry` | body | `string` | no | Expiration timestamp for the link. |
| `id` | path | `number` | yes | Link ID to update. |
| `metadescription` | body | `string` | no | Meta description for the link. |
| `metaimage` | body | `string` | no | URL to a JPG or PNG image. |
| `metatitle` | body | `string` | no | Meta title for the link. |
| `password` | body | `string` | no | Password protection for the link. |
| `type` | body | `string` | no | Redirection type such as direct, frame, or splash. |
| `url` | body | `string` | yes | Long URL for the link. |
| `geotarget` | body | `object` | no | Geo targeting data. |
| `devicetarget` | body | `object` | no | Device targeting data. |
| `languagetarget` | body | `object` | no | Language targeting data. |
| `pixels[]` | body | `array<number>` | no | Array of pixel IDs. |
| `deeplink` | body | `object` | no | Object containing app store links. |
