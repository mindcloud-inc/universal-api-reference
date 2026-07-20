# Query Phonebook with PBX Yeastar

Retrieves a phonebook from PBX Yeastar.

## Endpoint

- **Method:** `GET`
- **Path:** `/phonebook/get`
- **Base URL:** `{baseUrl}/openapi/v1.0`
- **Official documentation:** [Query Phonebook](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-information-of-a-phonebook.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | Unique phonebook ID. |
