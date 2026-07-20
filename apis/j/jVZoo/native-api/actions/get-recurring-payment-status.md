# Get Recurring Payment Status with JVZoo

Retrieves recurring payment status from JVZoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring_payment/:preKey`
- **Base URL:** `https://api.jvzoo.com/v2.0`
- **Official documentation:** [Get Recurring Payment Status](https://api.jvzoo.com/docs/versions/v2.0.html#payments-recurring-payments-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preKey` | path | `string` | yes | The key used for the recurring payment. |
