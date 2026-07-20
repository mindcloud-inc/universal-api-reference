# Create Collection with LinkTwin

Creates a new collection in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/add`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Create Collection](https://linktw.in/developers#create-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Collection name. |
| `slug` | body | `string` | no | Rotator slug. |
| `description` | body | `string` | no | Collection description. |
| `color` | body | `string` | no | Collection badge color in HEX. |
| `public` | body | `boolean` | no | Whether the collection is public. |
| `starred` | body | `boolean` | no | Whether the collection is starred. |
