# <img src="https://images.mindcloud.co/apps/icons/one-hash-erp_1776782423141.png" alt="OneHash ERP logo" width="28" height="28"> OneHash ERP: Universal API

OneHash ERP wraps the OneHash Frappe/ERP REST API for customers, items, invoices, orders, stock, and related ERP records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneHashERP/latest
- **Category:** Commerce / ERP
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.onehash.ai/erp
- **Vendor API docs:** https://docs.frappe.io/framework/user/en/api/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneHashERP/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from OneHash ERP. |

