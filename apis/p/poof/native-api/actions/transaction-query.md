# Transaction Query with Poof

Retrieves transaction query results from Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction_query`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Transaction Query](https://docs.poof.io/reference/transaction_query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `string` | yes | Transaction query filter key. |
| `search` | body | `string` | yes | Transaction query search value. |
