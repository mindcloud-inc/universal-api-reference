# Néctar CRM: Native API Reference

A consolidated summary of Néctar CRM's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://nectarcrm.docs.apiary.io/
- **API base URL:** `https://app.nectarcrm.com.br/crm/api/1`

## Authentication

### API Key

Authenticate requests with the Nectar CRM API token in the Access-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Access-Token: <apiKey>
```

[Official authentication documentation](https://ajuda.nectarcrm.com.br/hc/pt-br/articles/5609368705939-Pluga)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `displayLength` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | `POST /compromissos/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/compromissos/criar) |
| [Create Contact](actions/create-contact.md) | `POST /contatos/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/contatos/criar) |
| [Create Task](actions/create-task.md) | `POST /tarefas/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/tarefas/criar) |
| [Get Appointment](actions/get-appointment.md) | `GET /compromissos/:id` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/compromissos/consultar) |
| [Get Contact](actions/get-contact.md) | `GET /contatos/:id` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/contatos/consultar-por-id) |
| [Get Task](actions/get-task.md) | `GET /tarefas/:id` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/tarefas/consultar) |
| [List Appointments](actions/list-appointments.md) | `GET /compromissos/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/compromissos/listar) |
| [List Contacts](actions/list-contacts.md) | `GET /contatos/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/contatos/listar-contatos) |
| [List Opportunities](actions/list-opportunities.md) | `GET /oportunidades/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/oportunidades/listar) |
| [List Origins](actions/list-origins.md) | `GET /origem/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/origem/listar) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipeline/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/pipeline/listar-funil) |
| [List Products](actions/list-products.md) | `GET /produto/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/produtos/listar) |
| [List Qualifications](actions/list-qualifications.md) | `GET /qualificacoes/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/qualificacoes/listar) |
| [List Segments](actions/list-segments.md) | `GET /segmento/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/segmento/listar) |
| [List Tags](actions/list-tags.md) | `GET /lista/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/tags-lista/listar) |
| [List Tasks](actions/list-tasks.md) | `GET /tarefas/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/tarefas/listar) |
| [List Users](actions/list-users.md) | `GET /usuarios/` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/usuario/listar) |
| [Search Contacts by Email](actions/search-contacts-by-email.md) | `GET /contatos/email/:email` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/contatos/consultar-por-email) |
| [Update Appointment](actions/update-appointment.md) | `PUT /compromissos/:id` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/compromissos/editar) |
| [Update Contact](actions/update-contact.md) | `PUT /contatos/:id` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/contatos/editar) |
| [Update Task](actions/update-task.md) | `PUT /tarefas/:id` | [docs](https://nectarcrm.docs.apiary.io/#reference/0/tarefas/editar) |
