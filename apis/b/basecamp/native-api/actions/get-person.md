# Get Person with Basecamp

Retrieves a person from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/people/:personId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Person](https://github.com/basecamp/bc3-api/blob/master/sections/people.md#get-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID. |
| `personId` | path | `number` | yes | Basecamp person ID. |
