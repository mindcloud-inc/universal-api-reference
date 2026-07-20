# Request Phone Number Info In Path with TeleSign

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/phoneid/{complete_phone_number}`
- **Base URL:** `https://rest-ww.telesign.com`
- **Official documentation:** [Request Phone Number Info In Path](https://developer.telesign.com/enterprise/reference/submitphonenumberforidentity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `complete_phone_number` | path | `string` | yes |
| `account_lifecycle_event` | body | `string` | yes |
| `originating_ip` | body | `string` | yes |
