# Get Prospect Status By Email with Klenty

Retrieves prospect status from Klenty by email.

## Endpoint

- **Method:** `GET`
- **Path:** `/prospects/{{email}}/status`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Get Prospect Status By Email](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_82c37984ec)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email address. |
