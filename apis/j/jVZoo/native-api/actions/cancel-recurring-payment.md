# Cancel Recurring Payment with JVZoo

Cancels a recurring payment in JVZoo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recurring_payment/:preKey`
- **Base URL:** `https://api.jvzoo.com/v2.0`
- **Official documentation:** [Cancel Recurring Payment](https://api.jvzoo.com/docs/versions/v2.0.html#payments-recurring-payments-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preKey` | path | `string` | yes | The key used for the recurring payment. |
