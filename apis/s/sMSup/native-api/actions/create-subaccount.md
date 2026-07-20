# Create Subaccount with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/subaccount/create`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Create Subaccount](https://app.smsup.es/api/3.0/docs/subaccount/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_name` | body | `string` | yes | Username for the subaccount. |
| `email` | body | `string` | yes | Email for the subaccount. |
| `name` | body | `string` | yes | First name of the subaccount user. |
| `surname` | body | `string` | yes | Surname of the subaccount user. |
| `password` | body | `string` | yes | Password for the subaccount. |
| `language` | body | `string` | yes | Subaccount language. |
| `enable_shortener` | body | `number` | no | Set to 1 to enable shortener features on the subaccount. |
