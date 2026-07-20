# Get Recording with Sipuni

Retrieves a call recording audio file from Sipuni.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistic/record`
- **Base URL:** `https://sipuni.com/api`
- **Official documentation:** [Get Recording](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Recording ID from the exported statistics CSV. |
