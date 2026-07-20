# <img src="https://images.mindcloud.co/apps/icons/id3j1cckov-1775757159638_1775757164148.jpeg" alt="Snappy logo" width="28" height="28"> Snappy: Universal API

Snappy is a corporate gifting platform for sending gift collections, swag, and experiences to employees, customers, and prospects.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/snappy/latest
- **Category:** Commerce
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.snappy.com
- **Vendor API docs:** https://docs.snappy.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Keys](actions/get-api-keys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Snappy. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Snappy. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Snappy. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Order Address](actions/autocomplete-order-address.md) | GET | Finds shipping address suggestions in Snappy by partial input. |
| [Validate Order Address](actions/validate-order-address.md) | GET | Validates a shipping address in Snappy. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Snappy. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an existing API key from Snappy. |
| [Get API Keys](actions/get-api-keys.md) | GET | Retrieves API keys from Snappy. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Snappy. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Snappy. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Snappy. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Snappy. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Snappy. |

### Collection Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Product](actions/get-collection-product.md) | GET | Retrieves a product from a specific Snappy collection. |
| [List Collection Products](actions/list-collection-products.md) | GET | Retrieves products from a specific Snappy collection. |

### Demo Gift

| Action | Method | Description |
| --- | --- | --- |
| [Create Demo Gift](actions/create-demo-gift.md) | POST | Creates a non-claimable demo gift in Snappy. |

### Estimated Cost

| Action | Method | Description |
| --- | --- | --- |
| [Get Estimated Cost](actions/get-estimated-cost.md) | GET | Retrieves a campaign cost estimate from Snappy. |

### Gift

| Action | Method | Description |
| --- | --- | --- |
| [Claim Gift](actions/claim-gift.md) | PUT | Claims an existing gift in Snappy. |
| [Create Gifts](actions/create-gifts.md) | POST | Creates one or more gifts in Snappy. |
| [Expire Gift](actions/expire-gift.md) | PUT | Expires an existing unclaimed gift in Snappy. |
| [Get Gift](actions/get-gift.md) | GET | Retrieves a gift from Snappy. |
| [List Gifts](actions/list-gifts.md) | GET | Retrieves gifts from Snappy. |
| [Update Gift](actions/update-gift.md) | PUT | Updates an existing unclaimed gift in Snappy. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Snappy. |

### Product Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Product Tags](actions/list-product-tags.md) | GET | Retrieves product tags from Snappy. |

### Product Variant

| Action | Method | Description |
| --- | --- | --- |
| [Get Variant](actions/get-variant.md) | GET | Retrieves a variant from Snappy. |
| [List Product Variants](actions/list-product-variants.md) | GET | Retrieves variants for a product from Snappy. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new recipient in Snappy. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an existing recipient from Snappy. |
| [Get Recipient](actions/get-recipient.md) | GET | Retrieves a recipient from Snappy. |
| [List Recipients](actions/list-recipients.md) | GET | Retrieves recipients from Snappy. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in Snappy. |

