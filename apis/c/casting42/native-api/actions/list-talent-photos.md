# List Talent Photos with Casting42

Retrieves photos for a Casting42 talent.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/talents/photos/{{talentTag}}/medium`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [List Talent Photos](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `talentTag` | path | `string` | yes | Unique tag of the talent whose photos you want to fetch. |
