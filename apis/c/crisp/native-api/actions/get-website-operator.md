# Get Website Operator with Crisp

Retrieves a website operator from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/operator/:user_id`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Website Operator](https://docs.crisp.chat/references/rest-api/v1/#get-a-website-operator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `user_id` | path | `string` | yes | The user identifier for operator |
