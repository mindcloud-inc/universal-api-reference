# <img src="https://images.mindcloud.co/apps/icons/botbaba-mascot-150x150_1776093584848.png" alt="Botbaba logo" width="28" height="28"> Botbaba: Universal API

Build and manage WhatsApp and web chatbots, bot users, conversations, tags, products, and eCommerce automation data in Botbaba.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botbaba/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://botbaba.io/
- **Vendor API docs:** https://app.botbaba.io/swagger/ui/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Block

| Action | Method | Description |
| --- | --- | --- |
| [Get Blocks](actions/get-blocks.md) | GET |  |

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET |  |

### Bot Widget Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot Widget Settings](actions/get-bot-widget-settings.md) | GET |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Conversations](actions/list-bot-conversations.md) | GET |  |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [Update Product Inventory](actions/update-product-inventory.md) | PUT |  |
| [Update Product Inventory Total](actions/update-product-inventory-total.md) | PUT |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Set Product Active Status](actions/set-product-active-status.md) | PUT |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Product Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Category](actions/create-product-category.md) | POST |  |
| [Get Product Category](actions/get-product-category.md) | GET |  |
| [List Product Categories](actions/list-product-categories.md) | GET |  |
| [Set Product Category Active Status](actions/set-product-category-active-status.md) | PUT |  |
| [Update Product Category](actions/update-product-category.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Tags](actions/list-bot-tags.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot User](actions/create-bot-user.md) | POST |  |
| [Get Bot User](actions/get-bot-user.md) | GET |  |

### User Field

| Action | Method | Description |
| --- | --- | --- |
| [List User Fields](actions/list-user-fields.md) | GET |  |

