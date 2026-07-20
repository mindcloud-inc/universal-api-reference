# Perform an Email Validator request with Routee

Creates an email validator request in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/emailvalidator`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Perform an Email Validator request](https://docs.routee.net/reference/perform-an-email-validator-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | This is the email address to perform the validation. |
| `label` | body | `string` | no | This is the label that will be given to tag a specific Email Validation request. |
