# List Event Sources with SIGNL4

Retrieves event sources from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/eventsources`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [List Event Sources](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId[]` | query | `array<string>` | no | Team Ids to get the event sources from. If you don't add any team id, you get event sources you have access to from your subscription. |
| `includeInternal` | query | `boolean` | no | If true internal Event Sources type (System, Manual, API) will be included in the result. |
| `language` | query | `number` | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |
