# Pause Rebill with Explodely

Updates a rebill in Explodely by delaying the next charge.

## Endpoint

- **Method:** `GET`
- **Path:** `/rebill`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Pause Rebill](https://docs.explodely.com/api/pause-rebill-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mainorderid` | query | `string` | yes | The initial Explodely order ID for the rebill sale. |
| `delaydays` | query | `string` | yes | The number of days to delay the next rebill, up to 30. |
