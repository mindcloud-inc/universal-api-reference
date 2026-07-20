# Create holdout with Statsig

Creates a holdout in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/holdouts`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create holdout](https://docs.statsig.com/api-reference/holdouts/create-holdout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `idType` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
