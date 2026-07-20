# <img src="https://images.mindcloud.co/apps/icons/idiizt-btz-o-logos_1774368524483.jpeg" alt="Zakeke logo" width="28" height="28"> Zakeke: Universal API

Visual commerce platform for product customization, 3D configuration, orders, designs, and compositions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zakeke/latest
- **Category:** Commerce
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zakeke.com/
- **Vendor API docs:** https://docs.zakeke.com/docs/API/Introduction-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Seller Setup Status](actions/retrieve-seller-setup-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-seller-setup-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Count Designs](actions/count-designs.md) | GET |  |
| [Duplicate Design](actions/duplicate-design.md) | POST |  |
| [Retrieve Design By ID](actions/retrieve-design-by-id.md) | GET |  |
| [Retrieve Design Items](actions/retrieve-design-items.md) | GET |  |
| [Retrieve Print-Ready File](actions/retrieve-print-ready-file.md) | GET |  |
| [Retrieve Print-Ready ZIP](actions/retrieve-print-ready-zip.md) | GET |  |

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Composition Cart Info](actions/retrieve-composition-cart-info.md) | GET |  |

### Csv Import Result

| Action | Method | Description |
| --- | --- | --- |
| [Check Import Status](actions/check-import-status.md) | GET |  |

### Csv Import Task

| Action | Method | Description |
| --- | --- | --- |
| [Import Products Via CSV](actions/import-products-via-csv.md) | POST |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Register Order](actions/register-order.md) | POST |  |
| [Retrieve Order By Code](actions/retrieve-order-by-code.md) | GET |  |
| [Retrieve Order By ID](actions/retrieve-order-by-id.md) | GET |  |

### Provider Product

| Action | Method | Description |
| --- | --- | --- |
| [Import Provider Products](actions/import-provider-products.md) | POST |  |
| [Update Provider Products](actions/update-provider-products.md) | PUT |  |

### Provider Product Template

| Action | Method | Description |
| --- | --- | --- |
| [Import Provider Product Templates](actions/import-provider-product-templates.md) | POST |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Seller Setup Status](actions/retrieve-seller-setup-status.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete Templates By Code](actions/delete-templates-by-code.md) | DELETE |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Composition By ID](actions/retrieve-composition-by-id.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Customers Who Created Compositions](actions/list-customers-who-created-compositions.md) | GET |  |
| [List Customers Who Created Designs](actions/list-customers-who-created-designs.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Register Webhook](actions/register-webhook.md) | POST |  |

