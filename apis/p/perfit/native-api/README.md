# Perfit: Native API Reference

A consolidated summary of Perfit's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developers.myperfit.com/
- **API base URL:** `https://api.myperfit.com/v2`

## Authentication

### API Key

Connect with a Perfit user API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authentication: <apiKey>
```

[Official authentication documentation](https://developers.myperfit.com/contacts-api/autenticacion)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `paging.next`.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Interest To Contact](actions/add-interest-to-contact.md) | `PUT /:account/contacts/:contactId/interests/:interest` | [docs](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/agregar-un-interes-a-un-contacto) |
| [Create Interest](actions/create-interest.md) | `POST /:account/interests` | [docs](https://developers.myperfit.com/contacts-api/introduccion) |
| [Create List](actions/create-list.md) | `POST /:account/lists` | [docs](https://developers.myperfit.com/contacts-api/introduccion) |
| [Create Or Update Contact In List](actions/create-or-update-contact-in-list.md) | `POST /:account/lists/:list/contacts` | [docs](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/crear-o-actualizar-un-contacto-en-una-lista) |
| [List Account Activity](actions/list-account-activity.md) | `GET /:account/activity` | [docs](https://developers.myperfit.com/monitoreo/listado-de-actividad) |
| [Send Custom Trigger Event](actions/send-custom-trigger-event.md) | `POST https://webhooks.myperfit.net/events/customtriggers/app4/init/764ac753/a033319a` | [docs](https://developers.myperfit.com/custom-triggers/activacion-y-envio-de-eventos) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST /:account/contacts/:contactId/unsubscribe` | [docs](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/desuscribir-a-un-contacto) |
| [Update Contact](actions/update-contact.md) | `PUT /:account/contacts/:contactId` | [docs](https://developers.myperfit.com/contacts-api/usos-mas-frecuentes/modificar-un-contacto-existente) |
