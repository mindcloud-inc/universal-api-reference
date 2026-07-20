# Update metadata attributes for multiple contacts with Maildrip

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contacts/bulk-attributes`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Update metadata attributes for multiple contacts](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIds[]` | body | `array<string>` | yes | Array of contact IDs to update (max 100) Send multiple values as a array. |
| `attributes` | body | `object` | yes | Object with attribute key-value pairs to update (max 10 attributes). Keys must be alphanumeric with underscores/hyphens (max 50 chars). Values must be primitives (max 500 chars). |
