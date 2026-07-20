# Create Statuspage with Pinghome

Creates a new statuspage in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/statuspage-cmd/v1/statuspage`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Statuspage](https://docs.pinghome.io/statuspages/create-statuspage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Statuspage name. |
| `description` | body | `string` | yes | Statuspage description. |
| `subdomain` | body | `string` | yes | Statuspage subdomain. |
| `type` | body | `string` | yes | Statuspage type. |
| `components` | body | `string` | yes | JSON array of components. |
| `groups` | body | `string` | yes | JSON array of groups. |
