# Create Label with Recommand

Creates a new label in Recommand.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/labels`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Create Label](https://recommand.eu/en/reference/labels/create-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `colorHex` | body | `string` | yes | colorHex body field. |
| `externalId` | body | `string` | no | externalId body field. |
| `name` | body | `string` | yes | name body field. |
