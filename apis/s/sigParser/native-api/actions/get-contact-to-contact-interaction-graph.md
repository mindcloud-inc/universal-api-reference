# Get Contact-to-Contact Interaction Graph with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts/ContactsGraph`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Get Contact-to-Contact Interaction Graph](https://ipaas.sigparser.com/v1#post-api-contacts-contactsgraph)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_email` | body | `string` | yes | Email address of the primary contact. |
| `related_contact_email` | body | `string` | yes | Email address of the related contact. |
| `start_date` | body | `date` | yes | Start date of the interactions. |
