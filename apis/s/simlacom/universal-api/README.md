# <img src="https://images.mindcloud.co/apps/icons/6256d5a617e5c087310d0e9e-icon-simla_1775075306950.png" alt="Simla.com logo" width="28" height="28"> Simla.com: Universal API

Omnichannel AI-powered CRM platform to automate communications, track team performance, and manage your customer database.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simlacom/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.simla.com/
- **Vendor API docs:** https://docs.simla.com/Developers/API/APIVersions/APIv5

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current API Credentials](actions/get-current-api-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simlacom/latest/actions/get-current-api-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Api Credentials

| Action | Method | Description |
| --- | --- | --- |
| [Get Current API Credentials](actions/get-current-api-credentials.md) | GET | Retrieves current API access details from Simla.com. |

### Cost Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Groups](actions/list-cost-groups.md) | GET | Retrieves cost group records from Simla.com. |

### Cost Items

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Items](actions/list-cost-items.md) | GET | Retrieves cost item records from Simla.com. |

### Countries

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves available country codes from Simla.com. |

### Couriers

| Action | Method | Description |
| --- | --- | --- |
| [List Couriers](actions/list-couriers.md) | GET | Retrieves courier reference records from Simla.com. |

### Currencies

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currency reference records from Simla.com. |

### Delivery Services

| Action | Method | Description |
| --- | --- | --- |
| [List Delivery Services](actions/list-delivery-services.md) | GET | Retrieves delivery service records from Simla.com. |

### Delivery Types

| Action | Method | Description |
| --- | --- | --- |
| [List Delivery Types](actions/list-delivery-types.md) | GET | Retrieves delivery type records from Simla.com. |

### Legal Entities

| Action | Method | Description |
| --- | --- | --- |
| [List Legal Entities](actions/list-legal-entities.md) | GET | Retrieves legal entity records from Simla.com. |

### Order Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Order Methods](actions/list-order-methods.md) | GET | Retrieves order method records from Simla.com. |

### Order Types

| Action | Method | Description |
| --- | --- | --- |
| [List Order Types](actions/list-order-types.md) | GET | Retrieves order type records from Simla.com. |

### Payment Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Statuses](actions/list-payment-statuses.md) | GET | Retrieves payment status records from Simla.com. |

### Payment Types

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Types](actions/list-payment-types.md) | GET | Retrieves payment type records from Simla.com. |

### Price Types

| Action | Method | Description |
| --- | --- | --- |
| [List Price Types](actions/list-price-types.md) | GET | Retrieves price type records from Simla.com. |

### Product Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Product Statuses](actions/list-product-statuses.md) | GET | Retrieves order item statuses from Simla.com. |

### Sites

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET | Retrieves site reference records from Simla.com. |

### Status Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Status Groups](actions/list-status-groups.md) | GET | Retrieves order status groups from Simla.com. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves order status records from Simla.com. |

### Stores

| Action | Method | Description |
| --- | --- | --- |
| [List Stores](actions/list-stores.md) | GET | Retrieves warehouse reference records from Simla.com. |

### Units

| Action | Method | Description |
| --- | --- | --- |
| [List Units](actions/list-units.md) | GET | Retrieves unit reference records from Simla.com. |

