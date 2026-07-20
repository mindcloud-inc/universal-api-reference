# List Account Users with White Swan

Retrieves account users from White Swan.

## Endpoint

- **Method:** `POST`
- **Path:** `/user`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [List Account Users](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/account-user-s)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | body | `string` | no | Optionally return one account user by email. |
