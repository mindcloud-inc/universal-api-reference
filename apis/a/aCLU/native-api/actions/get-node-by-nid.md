# Get Node By NID with ACLU

Retrieves a Torture Database node by numeric ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/fullnode/retrieve.json`
- **Base URL:** `https://www.thetorturedatabase.org/rest`
- **Official documentation:** [Get Node By NID](https://www.thetorturedatabase.org/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nid` | query | `number` | yes | Numeric Drupal node ID (nid). |
