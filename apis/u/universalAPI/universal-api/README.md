# <img src="https://images.mindcloud.co/apps/icons/universal-api_1776802635527.png" alt="Universal API logo" width="28" height="28"> Universal API: Universal API

Universal API (UAPI) provides a unified API layer for platform, HRIS, asset management, MDM, shipment, distributor, ATS, consumer, webhook, and connection resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/universalAPI/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://universalapi.io
- **Vendor API docs:** https://docs.universalapi.io/reference/introduction-2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Consumers](actions/list-consumers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-consumers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST | Authenticates with Universal API and retrieves an access token. |

### Am Order

| Action | Method | Description |
| --- | --- | --- |
| [List AM Orders](actions/list-am-orders.md) | GET | Retrieves asset management orders from Universal API. |

### Apn Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Get APN Certificate](actions/get-apn-certificate.md) | GET | Retrieves an APN certificate from Universal API. |

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [List Budgets](actions/list-budgets.md) | GET | Retrieves a list of budgets from Universal API. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | GET | Retrieves a connection from Universal API. |
| [List Connections](actions/list-connections.md) | GET | Retrieves a list of connections from Universal API. |

### Consumer

| Action | Method | Description |
| --- | --- | --- |
| [Create Consumer](actions/create-consumer.md) | POST | Creates a new consumer in Universal API. |
| [Delete Consumer](actions/delete-consumer.md) | DELETE | Deletes an existing consumer from Universal API. |
| [Get Consumer](actions/get-consumer.md) | GET | Retrieves a consumer from Universal API. |
| [List Consumers](actions/list-consumers.md) | GET | Retrieves a list of consumers from Universal API. |

### Device App

| Action | Method | Description |
| --- | --- | --- |
| [List Device Apps](actions/list-device-apps.md) | GET | Retrieves apps for a device from Universal API. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Disable Lost Mode](actions/disable-lost-mode.md) | PUT | Disables lost mode for a device in Universal API. |
| [Enable Lost Mode](actions/enable-lost-mode.md) | PUT | Enables lost mode for a device in Universal API. |
| [List Devices](actions/list-devices.md) | GET | Retrieves a list of devices from Universal API. |
| [Lock Device](actions/lock-device.md) | PUT | Locks an existing device in Universal API. |

### Distributor Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Distributor Order](actions/create-distributor-order.md) | POST | Creates a new distributor order in Universal API. |
| [Get Distributor Order](actions/get-distributor-order.md) | GET | Retrieves a distributor order from Universal API. |
| [List Distributor Orders](actions/list-distributor-orders.md) | GET | Retrieves distributor orders from Universal API. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get HRIS Employee](actions/get-hris-employee.md) | GET | Retrieves an HRIS employee from Universal API. |
| [List AM Employees](actions/list-am-employees.md) | GET | Retrieves asset management employees from Universal API. |
| [List HRIS Employees](actions/list-hris-employees.md) | GET | Retrieves HRIS employees from Universal API. |

### Equipment Item

| Action | Method | Description |
| --- | --- | --- |
| [List Equipment Items](actions/list-equipment-items.md) | GET | Retrieves equipment items from Universal API. |

### Login

| Action | Method | Description |
| --- | --- | --- |
| [SSO Login](actions/sso-login.md) | GET | Retrieves an SSO login URL from Universal API. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Universal API. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Universal API. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Track Shipment](actions/track-shipment.md) | GET | Retrieves tracking statuses for a shipment from Universal API. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get SSO Profile](actions/get-sso-profile.md) | GET | Retrieves an SSO profile from Universal API. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Universal API. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Universal API. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Universal API. |

