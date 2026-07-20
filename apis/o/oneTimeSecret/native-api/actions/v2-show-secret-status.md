# Show Secret Status with One-Time Secret

Retrieves a secret's status from One-Time Secret without consuming it.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/secret/:identifier/status`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Show Secret Status](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_secret_showsecretstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Secret identifier whose status should be retrieved. |
