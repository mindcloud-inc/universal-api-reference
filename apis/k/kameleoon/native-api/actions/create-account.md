# Create account with Kameleoon

## Endpoint

- **Method:** `POST`
- **Path:** `accounts`
- **Base URL:** `https://api.kameleoon.com`
- **Official documentation:** [Create account](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/create-account/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email associated with the account. |
| `firstName` | body | `string` | yes | First name of the account user. |
| `lastName` | body | `string` | yes | Last name of the account user. |
| `password` | body | `string` | yes | Password for the account. |
| `passwordConfirm` | body | `string` | yes | Password confirmation. |
