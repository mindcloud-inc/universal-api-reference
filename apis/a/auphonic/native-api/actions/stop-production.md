# Stop Production with Auphonic

Stops a production in Auphonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/production/:uuid/stop.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Stop Production](https://auphonic.com/help/api/update.html#further-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the production. |
