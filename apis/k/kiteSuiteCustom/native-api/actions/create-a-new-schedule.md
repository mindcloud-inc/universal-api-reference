# Create a new schedule with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaign/schedule`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create a new schedule](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | The name of the schedule. |
| `campaign` | body | `string` | yes | The ID of the campaign associated with the schedule. |
