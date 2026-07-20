# Get Contact By Email with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts/List`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Get Contact By Email](https://ipaas.sigparser.com/v1#post-api-contacts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailaddress` | body | `string` | yes | Find a single contact record by exact lowercase email address. |
