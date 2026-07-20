# Verify Lead with Lead Identity Check

## Endpoint

- **Method:** `POST`
- **Path:** `/main/lic/v1`
- **Base URL:** `https://leadidentitycheck-node.vercel.app`
- **Official documentation:** [Verify Lead](https://leadidentitycheck.com/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Firstname` | body | `string` | yes | Lead first name. |
| `Lastname` | body | `string` | yes | Lead last name. |
| `Phone` | body | `string` | yes | Lead phone number. |
| `Email` | body | `string` | no | Lead email address. |
| `Address` | body | `object` | no | Optional object with Street, City, State, and Zipcode keys. |
