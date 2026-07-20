# <img src="https://images.mindcloud.co/apps/icons/printone-postcards_1774973397616.png" alt="Print.one Postcards logo" width="28" height="28"> Print.one Postcards: Universal API

Send, personalize, and manage postcards

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/printonePostcards/latest
- **Category:** Marketing
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://print.one
- **Vendor API docs:** https://api.print.one/docs/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Company](actions/get-my-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-my-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch](actions/create-batch.md) | POST | Creates a new batch in Print.one Postcards. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch from Print.one Postcards. |
| [Get Batch Stats](actions/get-batch-stats.md) | GET | Retrieves batch statistics from Print.one Postcards. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches from Print.one Postcards. |
| [Update Batch](actions/update-batch.md) | PUT | Updates an existing batch in Print.one Postcards. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Archive Batch](actions/archive-batch.md) | DELETE | Archives an existing batch in Print.one Postcards. |
| [Cancel Batch](actions/cancel-batch.md) | DELETE | Cancels an existing batch in Print.one Postcards. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get My Company](actions/get-my-company.md) | GET | Retrieves your company details from Print.one Postcards. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Countries](actions/list-supported-countries.md) | GET | Retrieves supported countries from Print.one Postcards. |

### Custom File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Custom File](actions/delete-custom-file.md) | DELETE | Deletes an existing custom file from Print.one Postcards. |
| [Download Custom File](actions/download-custom-file.md) | GET | Downloads a custom file from Print.one Postcards. |
| [List Custom Files](actions/list-custom-files.md) | GET | Retrieves custom files from Print.one Postcards. |
| [Upload Custom File](actions/upload-custom-file.md) | POST | Uploads a custom file to Print.one Postcards. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Add Orders To Batch](actions/add-orders-to-batch.md) | POST | Adds orders to a batch in Print.one Postcards. |
| [Cancel Order](actions/cancel-order.md) | DELETE | Cancels an existing order in Print.one Postcards. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Print.one Postcards. |
| [Get Batch Order](actions/get-batch-order.md) | GET | Retrieves a batch order from Print.one Postcards. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Print.one Postcards. |
| [List Batch Orders](actions/list-batch-orders.md) | GET | Retrieves batch orders from Print.one Postcards. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Print.one Postcards. |

### Order Preview

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Preview](actions/get-order-preview.md) | GET | Retrieves an order PDF preview from Print.one Postcards. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch CSV Import](actions/cancel-batch-csv-import.md) | DELETE | Cancels a batch CSV import in Print.one Postcards. |
| [Cancel Batch Order](actions/cancel-batch-order.md) | DELETE | Cancels a batch order in Print.one Postcards. |
| [Get Batch CSV Import Details](actions/get-batch-csv-import-details.md) | GET | Retrieves batch CSV import details from Print.one Postcards. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Print.one Postcards. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Print.one Postcards. |
| [Duplicate Template](actions/duplicate-template.md) | POST | Creates a duplicate template in Print.one Postcards. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Print.one Postcards. |
| [List Template Versions](actions/list-template-versions.md) | GET | Retrieves template versions from Print.one Postcards. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Print.one Postcards. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Print.one Postcards. |

### Template Preview

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Preview](actions/create-template-preview.md) | POST | Creates a new template preview in Print.one Postcards. |
| [Get Template Preview](actions/get-template-preview.md) | GET | Retrieves a template preview from Print.one Postcards. |
| [Get Template Preview Details](actions/get-template-preview-details.md) | GET | Retrieves template preview details from Print.one Postcards. |

