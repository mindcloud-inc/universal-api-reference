# Get Transaction Summary with JVZoo

Retrieves a transaction summary from JVZoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions/summaries/:paykey`
- **Base URL:** `https://api.jvzoo.com/v2.0`
- **Official documentation:** [Get Transaction Summary](https://api.jvzoo.com/docs/versions/v2.0.html#transactions-transaction-summaries-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paykey` | path | `string` | yes | The payKey for the transaction you want JVZoo to summarize. |
