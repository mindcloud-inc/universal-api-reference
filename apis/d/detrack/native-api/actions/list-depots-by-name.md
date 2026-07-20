# List Depots By Name with Detrack

Finds depots in Detrack by depot name.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/depots`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [List Depots By Name](https://detrackapiv2.docs.apiary.io/#reference/depots/retrieve-depot-by-name/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Depot name. |
