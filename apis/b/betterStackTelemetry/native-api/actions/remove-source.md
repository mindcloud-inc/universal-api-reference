# Remove Source with Better Stack Telemetry

Deletes an existing telemetry source from Better Stack Telemetry.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/sources/:source_id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Remove Source](https://betterstack.com/docs/logs/api/delete-an-existing-source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | ID of the source to remove |
