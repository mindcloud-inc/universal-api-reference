# <img src="https://t2.gstatic.com/faviconV2?client=SOCIAL&type=FAVICON&fallback_opts=TYPE,SIZE,URL&url=https://www.avalara.com/us/en/index.html&size=48" alt="Avalara AvaTax logo" width="28" height="28"> Avalara AvaTax: Universal API

Your end-to-end solution for tax compliance. Make tax calculation faster, easier, and more accurate.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/avalara/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.avalara.com/us/en/products.html
- **Vendor API docs:** https://developer.avalara.com/api-reference/avatax/rest/v2/methods/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Connection](actions/test-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Code Types

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Code Types](actions/list-tax-code-types.md) | GET |  |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [Query Companies](actions/query-companies.md) | GET |  |

### Countries

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET |  |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET |  |
| [Query Customers](actions/query-customers.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET |  |
| [List Items By Company](actions/list-items-by-company.md) | GET |  |

### Jurisdictions Hierarchy

| Action | Method | Description |
| --- | --- | --- |
| [List Jurisdictions Hierarchy](actions/list-jurisdictions-hierarchy.md) | GET |  |

### Nexus

| Action | Method | Description |
| --- | --- | --- |
| [Get Nexus](actions/get-nexus.md) | GET |  |
| [List Nexus By Company](actions/list-nexus-by-company.md) | GET |  |

### Parameters

| Action | Method | Description |
| --- | --- | --- |
| [List Parameters](actions/list-parameters.md) | GET |  |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Test Connection](actions/test-connection.md) | GET |  |

### Tax Authority Types

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Authority Types](actions/list-tax-authority-types.md) | GET |  |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Code](actions/get-tax-code.md) | GET |  |
| [List Tax Codes By Company](actions/list-tax-codes-by-company.md) | GET |  |
| [Query Tax Codes](actions/query-tax-codes.md) | GET |  |

### Tax Rules

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Rules](actions/list-tax-rules.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST |  |
| [Get Transaction By Code](actions/get-transaction-by-code.md) | GET |  |
| [Get Transaction By Id](actions/get-transaction-by-id.md) | GET |  |
| [List Transactions By Company](actions/list-transactions-by-company.md) | GET |  |

### Use Codes

| Action | Method | Description |
| --- | --- | --- |
| [List Entity Use Codes](actions/list-entity-use-codes.md) | GET |  |

