# Create Customer Event with ProfitWell

Creates a customer event in ProfitWell.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.profitwell-events.com/dotjs/v1/customer/event`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Create Customer Event](https://classic.paddle.com/profitwell/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | The customer ID. |
