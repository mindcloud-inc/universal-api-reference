# Get SMS Status By Client Message ID with TextingHouse

Retrieves TextingHouse SMS status by client message ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/do`
- **Base URL:** `https://api.textinghouse.com/http/v1`
- **Official documentation:** [Get SMS Status By Client Message ID](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-demstatut)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `climsgid` | body | `string` | yes | Client-defined message identifier used for later status lookups. Maximum length: 32. |
