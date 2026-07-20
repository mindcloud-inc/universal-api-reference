# Create Filter with TrueMail

Creates a new blocklist filter in TrueMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/filters`
- **Base URL:** `https://api.mailcop.net`
- **Official documentation:** [Create Filter](https://mailcop.net/docs/api-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_type` | body | `string` | yes | The type of filter to create. Accepted values: `0`, `1`, `2`. |
| `value` | body | `string` | yes | The email, domain, or IP address to block. |
| `reason` | body | `string` | no | Optional reason for the filter entry. |
