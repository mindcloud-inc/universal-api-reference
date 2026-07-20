# Get Docket with GSA Public Comment

Retrieves a specific docket from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/dockets/:docketId`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [Get Docket](https://open.gsa.gov/api/regulationsgov/#detailed-information-for-a-single-docket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docketId` | path | `string` | yes | ID of the docket to return. |
