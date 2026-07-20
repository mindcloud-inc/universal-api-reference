# Create Custom Data Record with Virtually

Creates a new custom data record in Virtually.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgId/customData`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Create Custom Data Record](https://app.tryvirtually.com/api/docs#/Custom%20Data/CustomDataController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | The custom data records to create. |
| `data[].memberId` | body | `string` | yes | The member ID. |
| `data[].ts` | body | `number` | no | Optional event timestamp. |
| `data[].event` | body | `string` | no | Optional event name. |
| `data[].properties` | body | `object` | yes | Custom properties. |
