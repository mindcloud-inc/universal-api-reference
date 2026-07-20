# <img src="https://images.mindcloud.co/apps/icons/notificaes-inteligentes_1775857010052.png" alt="Notificações Inteligentes logo" width="28" height="28"> Notificações Inteligentes: Universal API

API do Notificações Inteligentes para controle das integrações.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/notificaesInteligentes/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://notificacoesinteligentes.com
- **Vendor API docs:** https://docs.notificacoesinteligentes.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Integrations](actions/list-integrations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Address](actions/lookup-address.md) | GET | Retrieves an address from Notificações Inteligentes by postal code. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Abandoned Cart Event](actions/send-abandoned-cart-event.md) | POST | Creates an abandoned cart event in Notificações Inteligentes. |
| [Send Billet Printed Event](actions/send-billet-printed-event.md) | POST | Creates a billet printed event in Notificações Inteligentes. |
| [Send Order Canceled Event](actions/send-order-canceled-event.md) | POST | Creates an order canceled event in Notificações Inteligentes. |
| [Send Order Delivered Event](actions/send-order-delivered-event.md) | POST | Creates an order delivered event in Notificações Inteligentes. |
| [Send Order Fulfilled Event](actions/send-order-fulfilled-event.md) | POST | Creates an order fulfilled event in Notificações Inteligentes. |
| [Send Order Paid Event](actions/send-order-paid-event.md) | POST | Creates an order paid event in Notificações Inteligentes. |
| [Send Order Processing Event](actions/send-order-processing-event.md) | POST | Creates an order processing event in Notificações Inteligentes. |
| [Send Order Refunded Event](actions/send-order-refunded-event.md) | POST | Creates an order refunded event in Notificações Inteligentes. |
| [Send Shipping Out For Delivery Event](actions/send-shipping-out-for-delivery-event.md) | POST | Creates a shipping out-for-delivery event in Notificações Inteligentes. |
| [Send Shipping Progress Event](actions/send-shipping-progress-event.md) | POST | Creates a shipping progress event in Notificações Inteligentes. |
| [Send Waiting Payment Event](actions/send-waiting-payment-event.md) | POST | Creates a waiting payment event in Notificações Inteligentes. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | POST | Creates a new integration in Notificações Inteligentes. |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Notificações Inteligentes by store ID. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Notificações Inteligentes. |
| [Update Integration](actions/update-integration.md) | PUT | Updates an existing integration in Notificações Inteligentes. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Notificações Inteligentes. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Notificações Inteligentes by ID. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Notificações Inteligentes. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Notificações Inteligentes. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Notificações Inteligentes. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Notificações Inteligentes by ID. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Notificações Inteligentes. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Notificações Inteligentes. |

