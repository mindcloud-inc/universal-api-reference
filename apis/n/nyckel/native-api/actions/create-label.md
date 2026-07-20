# Create Label with Nyckel

Creates a new label in Nyckel.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/:functionId/labels`
- **Base URL:** `https://www.nyckel.com/v1`
- **Official documentation:** [Create Label](https://www.nyckel.com/docs#create-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `name` | body | `string` | yes | Label name. |
| `description` | body | `string` | no | Optional label description. |
| `metadata` | body | `object` | no | Optional label metadata object. |
