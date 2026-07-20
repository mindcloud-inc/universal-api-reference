# Search Contacts by Email with Néctar CRM

Finds contacts in Néctar CRM by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/contatos/email/:email`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Search Contacts by Email](https://nectarcrm.docs.apiary.io/#reference/0/contatos/consultar-por-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email address to search for. |
