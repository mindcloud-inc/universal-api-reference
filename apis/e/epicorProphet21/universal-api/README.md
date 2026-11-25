# <img src="https://images.mindcloud.co/apps/icons/epicor-prophet21_1791908894393.png" alt="Epicor Prophet 21 logo" width="28" height="28"> Epicor Prophet 21: Universal API

Connect to Epicor Prophet 21 to read customers, contacts, addresses, sales orders, quotes, order lines, and product groups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/epicorProphet21/latest
- **Category:** Commerce / ERP
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.epicor.com/en-us/industry-productivity-solutions/distribution/prophet-21/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Product Groups](actions/list-product-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/list-product-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | GET |  |
| [List Entity Addresses](actions/list-entity-addresses.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Entity Contacts](actions/list-entity-contacts.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET |  |
| [List Entity Customers](actions/list-entity-customers.md) | GET |  |

### Order Lines

| Action | Method | Description |
| --- | --- | --- |
| [List Order Lines](actions/list-order-lines.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Orders](actions/list-sales-orders.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Data View Metadata](actions/get-data-view-metadata.md) | GET |  |
| [Get Data View Record](actions/get-data-view-record.md) | GET |  |
| [Get Manifest Metadata](actions/get-manifest-metadata.md) | GET |  |
| [Get OData Table Metadata](actions/get-odata-table-metadata.md) | GET |  |
| [Get OData View Metadata](actions/get-odata-view-metadata.md) | GET |  |
| [List Data Views](actions/list-data-views.md) | GET |  |
| [List Manifest Collections](actions/list-manifest-collections.md) | GET |  |
| [List OData Tables](actions/list-odata-tables.md) | GET |  |
| [List OData Views](actions/list-odata-views.md) | GET |  |
| [List Product Groups](actions/list-product-groups.md) | GET |  |
| [Query Data View](actions/query-data-view.md) | GET |  |
| [Query Manifest Collection](actions/query-manifest-collection.md) | GET |  |
| [Query OData Table](actions/query-odata-table.md) | GET |  |
| [Query OData Table with Body](actions/query-odata-table-with-body.md) | GET |  |
| [Query OData View](actions/query-odata-view.md) | GET |  |
| [Query OData View with Body](actions/query-odata-view-with-body.md) | GET |  |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes](actions/list-quotes.md) | GET |  |

