# List CRM Contacts with Billetweb

Retrieves CRM contacts from your Billetweb account.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/contacts`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List CRM Contacts](https://www.billetweb.fr/bo/api.php#/api/crm/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_update` | query | `number` | no | Only return contacts updated after this Unix timestamp. |
| `since` | query | `number` | no | Only return contacts updated during the last N minutes. |
| `to` | query | `number` | no | Only return contacts modified before this Unix timestamp. |
| `email` | query | `string` | no | Filter by buyer email. |
| `segment` | query | `number` | no | Filter by CRM segment identifier. |
