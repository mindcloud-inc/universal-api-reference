# Update List with VoilaNorbert

Updates an existing list in VoilaNorbert.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:id`
- **Base URL:** `https://api.voilanorbert.com/2018-01-08`
- **Official documentation:** [Update List](https://api.voilanorbert.com/2018-01-08/#lists-list-items-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The list id to update. |
| `name` | body | `string` | yes | The new list name. |
