# <img src="https://images.mindcloud.co/apps/icons/s-mmcode_1778008185220.png" alt="SMMCode logo" width="28" height="28"> SMMCode: Universal API

SMMCode is a social media marketing panel API for listing services, placing orders, checking order status, and reading account balance.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMMCode/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://extended.smmcode.org
- **Vendor API docs:** https://extended.smmcode.org/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Services](actions/list-services.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get User Balance](actions/get-user-balance.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Add Order](actions/add-order.md) | POST |  |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Multiple Order Statuses](actions/get-multiple-order-statuses.md) | GET |  |
| [Get Order Status](actions/get-order-status.md) | GET |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET |  |

