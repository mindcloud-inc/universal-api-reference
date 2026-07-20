# Get Latest Transactions with JVZoo

Retrieves latest transactions across your JVZoo products.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest-transactions/[:paykey]`
- **Base URL:** `https://api.jvzoo.com/v2.0`
- **Official documentation:** [Get Latest Transactions](https://api.jvzoo.com/docs/versions/v2.0.html#transactions-latest-transactions-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paykey` | path | `string` | no | If provided, JVZoo starts after this payKey and does not include it in the results. |
