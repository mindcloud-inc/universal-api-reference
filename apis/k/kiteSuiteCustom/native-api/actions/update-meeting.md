# update meeting . with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/meeting/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [update meeting .](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Meeting ID |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `startDate` | body | `string` | yes | — |
| `endDate` | body | `string` | yes | — |
