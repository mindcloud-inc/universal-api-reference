# Create Group with Frontegg

Creates a new user group in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/groups/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Create Group](https://developers.frontegg.com/ciam/api/identity/user-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Group unique name. |
| `color` | body | `string` | no | Color for group display. |
| `description` | body | `string` | no | Group description. |
| `metadata` | body | `string` | no | Stringified JSON metadata. |
