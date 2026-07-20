# Notificações Inteligentes: Native API Reference

A consolidated summary of Notificações Inteligentes's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.notificacoesinteligentes.com/
- **API base URL:** `https://api.notificacoesinteligentes.com`

## Authentication

### API Key

Bearer API key authentication for Notificações Inteligentes.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ajuda.notificacoesinteligentes.com/pt-br/article/como-integrar-utilizando-a-api-aooa5/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | `POST /integrations` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Get Integration](actions/get-integration.md) | `GET /integrations/:store` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:lead` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tag` | [docs](https://docs.notificacoesinteligentes.com/) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://docs.notificacoesinteligentes.com/) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://docs.notificacoesinteligentes.com/) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Lookup Address](actions/lookup-address.md) | `GET /addresses/:postalCode` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Abandoned Cart Event](actions/send-abandoned-cart-event.md) | `POST /integrations/:store/events/abandoned-cart` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Billet Printed Event](actions/send-billet-printed-event.md) | `POST /integrations/:store/events/billet-printed` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Order Canceled Event](actions/send-order-canceled-event.md) | `POST /integrations/:store/events/order-canceled` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Order Delivered Event](actions/send-order-delivered-event.md) | `POST /integrations/:store/events/order-delivered` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Order Fulfilled Event](actions/send-order-fulfilled-event.md) | `POST /integrations/:store/events/order-fulfilled` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Order Paid Event](actions/send-order-paid-event.md) | `POST /integrations/:store/events/order-paid` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Order Processing Event](actions/send-order-processing-event.md) | `POST /integrations/:store/events/order-processing` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Order Refunded Event](actions/send-order-refunded-event.md) | `POST /integrations/:store/events/order-refunded` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Shipping Out For Delivery Event](actions/send-shipping-out-for-delivery-event.md) | `POST /integrations/:store/events/shipping-out-for-delivery` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Shipping Progress Event](actions/send-shipping-progress-event.md) | `POST /integrations/:store/events/shipping-progress` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Send Waiting Payment Event](actions/send-waiting-payment-event.md) | `POST /integrations/:store/events/waiting-payment` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Update Integration](actions/update-integration.md) | `PUT /integrations/:store` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/:lead` | [docs](https://docs.notificacoesinteligentes.com/) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:tag` | [docs](https://docs.notificacoesinteligentes.com/) |
