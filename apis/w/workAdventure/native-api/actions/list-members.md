# List members with WorkAdventure

Retrieves members from a WorkAdventure world.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/worlds/:worldSlug/members`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [List members](https://docs.workadventu.re/developer/inbound-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `worldSlug` | path | `string` | yes | The world slug from the WorkAdventure world URL. |
| `limit` | query | `number` | yes | Maximum number of records to return. The API requires this query parameter and allows up to 100. |
| `offset` | query | `number` | yes | Offset of the records returned. |
