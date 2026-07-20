# Create Subaccount with Seven

Creates a new subaccount in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/subaccounts?action=create`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Create Subaccount](https://docs.seven.io/en/rest-api/endpoints/subaccounts#create-subaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Full first and last name of the account owner. |
| `email` | body | `string` | yes | Email address of the account. |
