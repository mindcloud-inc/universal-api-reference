# Update Link with Recut URL Shortener

Updates an existing link in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/url/:id/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update Link](https://app.recut.in/developers#update-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | Custom domain for the short link. |
| `id` | path | `number` | yes | Link ID. |
| `password` | body | `string` | no | Password protection for the short link. |
| `type` | body | `string` | no | Redirection type or custom splash / CTA overlay identifier. |
| `url` | body | `string` | yes | Long URL to shorten. |
| `custom` | body | `string` | no | Custom alias instead of a random alias. |
| `description` | body | `string` | no | Note or description for the link. |
| `expiry` | body | `date` | no | Expiration timestamp in `YYYY-MM-DD HH:mm:ss` format. |
| `pixels[]` | body | `array<number>` | no | Array of pixel IDs. |
| `channel` | body | `number` | no | Channel ID to attach to the link. |
| `campaign` | body | `number` | no | Campaign ID to attach to the link. |
| `deeplink` | body | `object` | no | Object containing app store links and optional `auto` generation flag. |
| `geotarget[]` | body | `array<object>` | no | Geo targeting rules as an array of objects with `location` and `link`. |
| `devicetarget[]` | body | `array<object>` | no | Device targeting rules as an array of objects with `device` and `link`. |
| `languagetarget[]` | body | `array<object>` | no | Language targeting rules as an array of objects with `language` and `link`. |
| `metatitle` | body | `string` | no | Open Graph / social title. |
| `metadescription` | body | `string` | no | Open Graph / social description. |
| `metaimage` | body | `string` | no | Image URL for link previews. |
| `parameters[]` | body | `array<object>` | no | Additional URL parameters as an array of objects from the docs example. |
