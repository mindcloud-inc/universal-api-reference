# Cancel Rebill with Explodely

Cancels rebills in Explodely by main order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/rebill`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Cancel Rebill](https://docs.explodely.com/api/cancel-rebill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mainorderid` | query | `string` | yes | The initial Explodely order ID for the rebill sale. |
