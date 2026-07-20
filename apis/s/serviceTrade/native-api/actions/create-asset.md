# Create Asset with ServiceTrade

Creates a new asset in ServiceTrade.

## Endpoint

- **Method:** `POST`
- **Path:** `asset`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Create Asset](https://api.servicetrade.com/api/docs#resource-asset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | ServiceTrade asset definition type to create, such as location or grease_containment. |
| `locationId` | body | `number` | yes | Location that will own the new asset. |
| `properties.notes` | body | `string` | no | Notes property for asset definitions that support it. |
| `taskListId` | body | `number` | no | Task list to attach to the new asset. |
