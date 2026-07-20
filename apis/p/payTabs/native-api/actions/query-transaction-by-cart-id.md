# Query Transaction by Cart ID with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/query`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Query Transaction by Cart ID](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Query-Transaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cart_id` | body | `string` | yes | Merchant cart or order identifier to query. |
