# Create Link with KlipLink

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links`
- **Base URL:** `https://api.klipl.ink`
- **Official documentation:** [Create Link](https://docs.klipl.ink/api/links/create-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_url` | body | `string` | yes | The destination URL the short link should redirect to. |
| `title` | body | `string` | no | Optional title for the short link. |
