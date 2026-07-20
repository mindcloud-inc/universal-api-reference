# Shorten Link with Recut URL Shortener

Creates a shortened link in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/url/add`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Shorten Link](https://app.recut.in/developers#shorten-a-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Long URL to shorten. |
| `custom` | body | `string` | no | Custom alias instead of a random alias. |
| `status` | body | `string` | no | Link visibility: `public` or `private`. |
| `description` | body | `string` | no | Note or description for the link. |
| `type` | body | `string` | no | Redirection type or custom splash / CTA overlay identifier. |
| `password` | body | `string` | no | Password protection for the short link. |
| `domain` | body | `string` | no | Custom domain for the short link. |
| `expiry` | body | `date` | no | Expiration timestamp in `YYYY-MM-DD HH:mm:ss` format. |
| `metatitle` | body | `string` | no | Open Graph / social title. |
| `metadescription` | body | `string` | no | Open Graph / social description. |
| `metaimage` | body | `string` | no | Image URL for link previews. |
| `pixels[]` | body | `array<number>` | no | Array of pixel IDs. |
| `channel` | body | `number` | no | Channel ID to attach to the link. |
| `campaign` | body | `number` | no | Campaign ID to attach to the link. |
| `deeplink` | body | `object` | no | Object containing app store links and optional `auto` generation flag. |
| `geotarget[]` | body | `array<object>` | no | Geo targeting rules as an array of objects with `location` and `link`. |
| `devicetarget[]` | body | `array<object>` | no | Device targeting rules as an array of objects with `device` and `link`. |
| `languagetarget[]` | body | `array<object>` | no | Language targeting rules as an array of objects with `language` and `link`. |
| `parameters[]` | body | `array<object>` | no | Additional URL parameters as an array of objects from the docs example. |
