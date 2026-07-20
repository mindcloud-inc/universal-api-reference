# Upsert Contact with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Upsert Contact](https://ipaas.sigparser.com/v1#post-api-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailaddress` | body | `string` | yes | Required. Email address for the contact. |
| `firstname` | body | `string` | no | First name for the contact. |
| `lastname` | body | `string` | no | Last name for the contact. |
| `title` | body | `string` | no | Job title for the contact. |
