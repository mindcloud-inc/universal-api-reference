# Create Email Forward with redirect.pizza

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/email-forwards`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Create Email Forward](https://redirect.pizza/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias` | body | `string` | yes | Alias before the @ sign. Use * for a catch-all forward. |
| `domain` | body | `string` | yes | Domain that receives the forwarded email. |
| `destination` | body | `string` | yes | Destination email address. |
