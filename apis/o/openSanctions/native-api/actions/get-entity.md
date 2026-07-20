# Get Entity with OpenSanctions

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entity_id`
- **Base URL:** `https://api.opensanctions.org`
- **Official documentation:** [Get Entity](https://api.opensanctions.org/docs#/Data%20access/fetch_entity_entities__entity_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | ID of the entity to retrieve. OpenSanctions documents Q7747 as an example entity ID. |
| `nested` | query | `boolean` | no | Include adjacent entities such as addresses, family, passport, sanction, and associated entities in the response. |
