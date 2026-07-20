# Create or Update Contact with Trustmary

Finds a contact by email in Trustmary, or creates one if missing.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.trustmary.io/v1`
- **Official documentation:** [Create or Update Contact](https://help.trustmary.com/api#/paths/~1contacts/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address. |
| `name` | body | `string` | no | Contact full name. |
| `eid` | body | `string` | no | Your external identifier for the contact. |
| `phone` | body | `string` | no | Phone number with country code. |
| `company` | body | `string` | no | Company name. |
| `type` | body | `string` | no | Contact type: customer or employee. |
