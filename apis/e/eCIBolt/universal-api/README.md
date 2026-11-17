# <img src="https://images.mindcloud.co/apps/icons/e-cibolt_1794871522229.png" alt="ECI Bolt logo" width="28" height="28"> ECI Bolt: Universal API

Manage jobs, work orders, schedules, and customers in ECI Bolt

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eCIBolt/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ecisolutions.com/products/bolt-trade-contractor-software/
- **Vendor API docs:** https://app.bolttech.net/api-docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Stages](actions/list-stages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Community

| Action | Method | Description |
| --- | --- | --- |
| [Get Community](actions/get-community.md) | GET |  |
| [List Communities](actions/list-communities.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Job Events](actions/list-job-events.md) | GET |  |
| [List Work Order Events](actions/list-work-order-events.md) | GET |  |

### Event Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Event Token](actions/get-job-event-token.md) | GET |  |
| [Get Work Order Event Token](actions/get-work-order-event-token.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Stages](actions/list-stages.md) | GET |  |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Work Order](actions/create-work-order.md) | POST |  |
| [Get Work Order](actions/get-work-order.md) | GET |  |
| [List Job Work Orders](actions/list-job-work-orders.md) | GET |  |
| [List Work Orders](actions/list-work-orders.md) | GET |  |
| [Update Work Order](actions/update-work-order.md) | PUT |  |

### Work Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET |  |
| [List Work Order Statuses](actions/list-work-order-statuses.md) | GET |  |
| [Update Work Order Status](actions/update-work-order-status.md) | PUT |  |

### Work Order Type

| Action | Method | Description |
| --- | --- | --- |
| [List Work Order Types](actions/list-work-order-types.md) | GET |  |

