# Shorten Link with JmpTo

Creates a shortened link in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/url/add`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Shorten Link](https://jmpto.net/developers#shorten-a-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Note or description for the short link. |
| `metadescription` | body | `string` | no | Meta description for the short link. |
| `metaimage` | body | `string` | no | URL to a JPG or PNG image. |
| `metatitle` | body | `string` | no | Meta title for the short link. |
| `url` | body | `string` | yes | Long URL to shorten. |
| `custom` | body | `string` | no | Custom alias instead of a random alias. |
| `type` | body | `string` | no | Redirection type such as direct, frame, or splash. |
| `password` | body | `string` | no | Password protection for the short link. |
| `domain` | body | `string` | no | Custom domain for the short link. |
| `expiry` | body | `string` | no | Expiration timestamp for the link. |
| `geotarget` | body | `object` | no | Geo targeting data. |
| `devicetarget` | body | `object` | no | Device targeting data. |
| `languagetarget` | body | `object` | no | Language targeting data. |
| `pixels[]` | body | `array<number>` | no | Array of pixel IDs. |
| `channel` | body | `number` | no | Channel ID. |
| `campaign` | body | `number` | no | Campaign ID. |
| `deeplink` | body | `object` | no | Object containing app store links. |
| `status` | body | `string` | no | Link status, public or private. |
