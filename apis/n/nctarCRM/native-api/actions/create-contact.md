# Create Contact with Néctar CRM

Creates a new contact in Néctar CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contatos/`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Create Contact](https://nectarcrm.docs.apiary.io/#reference/0/contatos/criar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nome` | body | `string` | yes | Contact name. |
| `constante` | body | `number` | yes | Contact type: 0 client, 1 prospect, 2 suspect, 3 lead, 5 discarded. |
| `emails[]` | body | `array<string>` | no | Email addresses for the contact. |
