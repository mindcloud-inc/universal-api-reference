# List Position Shareable Links with Hireflix

Retrieves shareable links for a position in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [List Position Shareable Links](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix position ID. |
| `variables.shareableLinkId` | body | `string` | no | Optionally limit the response to a specific position shareable link ID. |
