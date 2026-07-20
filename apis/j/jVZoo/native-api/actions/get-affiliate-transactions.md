# Get Affiliate Transactions with JVZoo

Retrieves your latest affiliate transactions from JVZoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest-affiliates-transactions/[:paykey]`
- **Base URL:** `https://api.jvzoo.com/v2.0`
- **Official documentation:** [Get Affiliate Transactions](https://api.jvzoo.com/docs/versions/v2.0.html#transactions-affiliate-transactions-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paykey` | path | `string` | no | If provided, JVZoo starts after this payKey and does not include it in the results. |
