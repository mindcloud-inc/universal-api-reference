# Get Multiple Order Statuses with SMMCode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2`
- **Base URL:** `https://extended.smmcode.org`
- **Official documentation:** [Get Multiple Order Statuses](https://extended.smmcode.org/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders` | body | `string` | yes | Order IDs separated by commas. Send multiple values as a string separated by `,`. |
