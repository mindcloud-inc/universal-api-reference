# Update Stage0 Entry with Inistate

Updates an existing Stage0 entry in Inistate.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/activity`
- **Base URL:** `https://api.inistate.com`
- **Official documentation:** [Update Stage0 Entry](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryId` | body | `number` | yes | Entry to update. |
| `payload` | body | `object` | no | Optional field payload keyed by provider field names. An empty object performs the provider's default edit submission shape verified in this run. |
