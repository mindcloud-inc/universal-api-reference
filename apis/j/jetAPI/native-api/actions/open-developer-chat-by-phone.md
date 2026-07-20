# Open Developer Chat By Phone with JetAPI

Retrieves a developer chat link from JetAPI by phone.

## Endpoint

- **Method:** `GET`
- **Path:** `/developer_chat`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Open Developer Chat By Phone](https://docs.jetapi.io/#ca99f0ce-984e-40ee-ba7a-8678c240bea6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `number` | yes | Customer identifier for the developer chat. |
| `hash` | query | `string` | yes | Developer chat hash. |
| `phone` | query | `string` | yes | Phone number to open in the developer chat. |
