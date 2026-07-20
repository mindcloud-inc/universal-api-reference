# <img src="https://images.mindcloud.co/apps/icons/productifyai_1776802599117.png" alt="Productify.ai logo" width="28" height="28"> Productify.ai: Universal API

Productify.ai is an API-first product data platform for transforming product images, packaging, text, and tables into structured ecommerce content, including descriptions, categorization, translations, extraction, and batch workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productifyai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.productify.ai/
- **Vendor API docs:** https://api.productify.ai/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET |  |

### Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Digitisation Batch](actions/create-digitisation-batch.md) | POST |  |
| [Create Ecommerce Batch](actions/create-ecommerce-batch.md) | POST |  |
| [Create Generate Batch](actions/create-generate-batch.md) | POST |  |
| [Create Text Transform Batch](actions/create-text-transform-batch.md) | POST |  |

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Digitisation Batch Results](actions/get-digitisation-batch-results.md) | GET |  |
| [Get Digitisation Batch Results With GET](actions/get-digitisation-batch-results-with-get.md) | GET |  |
| [Get Ecommerce Batch Results](actions/get-ecommerce-batch-results.md) | GET |  |
| [Get Generate Batch Results](actions/get-generate-batch-results.md) | GET |  |
| [Get Generate Batch Results With GET](actions/get-generate-batch-results-with-get.md) | GET |  |
| [Get Text Transform Batch Results](actions/get-text-transform-batch-results.md) | GET |  |
| [Get Text Transform Batch Results With GET](actions/get-text-transform-batch-results-with-get.md) | GET |  |

### Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Status](actions/get-batch-status.md) | GET |  |

### Bonus Tier

| Action | Method | Description |
| --- | --- | --- |
| [List Bonus Tiers](actions/list-bonus-tiers.md) | GET |  |

### Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Perform Digitisation Extract](actions/perform-digitisation-extract.md) | POST |  |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Health](actions/check-health.md) | GET |  |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Languages](actions/list-supported-languages.md) | GET |  |

### Operation Cost

| Action | Method | Description |
| --- | --- | --- |
| [List Operation Costs](actions/list-operation-costs.md) | GET |  |

### Product Category

| Action | Method | Description |
| --- | --- | --- |
| [List Product Categories](actions/list-product-categories.md) | GET |  |

### Product Content

| Action | Method | Description |
| --- | --- | --- |
| [Perform Ecommerce Generate](actions/perform-ecommerce-generate.md) | POST |  |
| [Perform Generate](actions/perform-generate.md) | POST |  |

### System Test

| Action | Method | Description |
| --- | --- | --- |
| [Run System Test](actions/run-system-test.md) | GET |  |

### Taxonomy

| Action | Method | Description |
| --- | --- | --- |
| [List Taxonomies](actions/list-taxonomies.md) | GET |  |

### Text Transform Result

| Action | Method | Description |
| --- | --- | --- |
| [Perform Text Transform](actions/perform-text-transform.md) | POST |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Details](actions/get-workspace-details.md) | GET |  |

