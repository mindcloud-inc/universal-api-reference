# Update Label with Recommand

Updates an existing label in Recommand.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/labels/:labelId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Update Label](https://recommand.eu/en/reference/labels/update-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `colorHex` | body | `string` | no | colorHex body field. |
| `externalId` | body | `string` | no | externalId body field. |
| `labelId` | path | `string` | yes | labelId parameter. |
| `name` | body | `string` | no | name body field. |
