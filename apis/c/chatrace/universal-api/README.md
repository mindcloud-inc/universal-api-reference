# <img src="https://images.mindcloud.co/apps/icons/group_1781293086540.png" alt="Chatrace logo" width="28" height="28"> Chatrace: Universal API

Chatrace provides chatbot automation, contact management, pipeline, appointment, and ecommerce APIs for managing customer conversations and account resources across multiple messaging channels.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatrace/latest
- **Category:** Communication / Team Messaging
- **Actions:** 55
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chatrace.com
- **Vendor API docs:** https://docs.chatrace.com/kb/chatrace-api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Account Tags](actions/list-account-tags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-account-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (55)

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar record from Chatrace. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendar records from your Chatrace account. |

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Add Product To Cart](actions/add-product-to-cart.md) | POST | Adds a product to a Chatrace contact cart. |
| [Clear Contact Cart](actions/clear-contact-cart.md) | DELETE | Clears a contact cart in Chatrace. |
| [Get Contact Cart](actions/get-contact-cart.md) | GET | Retrieves a contact cart from Chatrace. |
| [Remove Product From Cart](actions/remove-product-from-cart.md) | DELETE | Removes a product from a Chatrace contact cart. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product record from Chatrace. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Chatrace. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity Comment](actions/create-opportunity-comment.md) | POST | Creates a new comment on a Chatrace opportunity. |
| [Delete Opportunity Comment](actions/delete-opportunity-comment.md) | DELETE | Deletes a comment from a Chatrace opportunity. |
| [List Opportunity Comments](actions/list-opportunity-comments.md) | GET | Retrieves comments from a Chatrace opportunity. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Chatrace. |
| [Find Contacts By Custom Field](actions/find-contacts-by-custom-field.md) | GET | Finds contacts in Chatrace by custom field value. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact record from Chatrace. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Order](actions/get-contact-order.md) | GET | Retrieves an order from a Chatrace contact. |
| [Mark Order As Paid](actions/mark-order-as-paid.md) | PUT | Marks a Chatrace contact order as paid. |
| [Update Contact Order](actions/update-contact-order.md) | PUT | Updates an order for a Chatrace contact. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | GET | Retrieves stages from a Chatrace pipeline. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Generate Template Link](actions/generate-template-link.md) | POST |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in Chatrace. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an opportunity record from Chatrace. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity record from Chatrace. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from a Chatrace pipeline. |
| [Transfer Opportunity To Pipeline](actions/transfer-opportunity-to-pipeline.md) | PUT | Transfers an opportunity to another Chatrace pipeline. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in Chatrace. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag To Contact](actions/add-tag-to-contact.md) | POST | Adds a tag to a contact in Chatrace. |
| [Create Account Custom Field](actions/create-account-custom-field.md) | POST | Creates a new account custom field in Chatrace. |
| [Create Account Tag](actions/create-account-tag.md) | POST | Creates a new account tag in Chatrace. |
| [Delete Account Tag](actions/delete-account-tag.md) | DELETE | Deletes an account tag from Chatrace. |
| [Get Account Custom Field](actions/get-account-custom-field.md) | GET | Retrieves an account custom field from Chatrace. |
| [Get Account Custom Field By Name](actions/get-account-custom-field-by-name.md) | GET | Finds an account custom field in Chatrace by name. |
| [Get Account Integrations](actions/get-account-integrations.md) | GET | Retrieves account integrations from your Chatrace account. |
| [Get Account Tag](actions/get-account-tag.md) | GET | Retrieves an account tag from Chatrace. |
| [Get Account Tag By Name](actions/get-account-tag-by-name.md) | GET | Finds an account tag in Chatrace by name. |
| [Get Bot Field Value](actions/get-bot-field-value.md) | GET | Retrieves a bot field value from Chatrace. |
| [Get Contact Custom Field](actions/get-contact-custom-field.md) | GET | Retrieves a custom field from a Chatrace contact. |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline record from Chatrace. |
| [List Account Custom Fields](actions/list-account-custom-fields.md) | GET | Retrieves account custom fields from Chatrace. |
| [List Account Flows](actions/list-account-flows.md) | GET | Retrieves account flows from your Chatrace account. |
| [List Account Tags](actions/list-account-tags.md) | GET | Retrieves account tags from your Chatrace account. |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | GET | Retrieves custom fields from a Chatrace contact. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves tags from a Chatrace contact. |
| [List Pipeline Custom Fields](actions/list-pipeline-custom-fields.md) | GET | Retrieves custom fields from a Chatrace pipeline. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipeline records from your Chatrace account. |
| [Remove Bot Field Value](actions/remove-bot-field-value.md) | DELETE | Removes a bot field value from Chatrace. |
| [Remove Contact Custom Field](actions/remove-contact-custom-field.md) | DELETE | Removes a custom field from a Chatrace contact. |
| [Remove Tag From Contact](actions/remove-tag-from-contact.md) | DELETE | Removes a tag from a Chatrace contact. |
| [Send Content To Contact](actions/send-content-to-contact.md) | POST | Sends content to a contact in Chatrace. |
| [Send File To Contact](actions/send-file-to-contact.md) | POST | Sends a file to a contact in Chatrace. |
| [Send Flow To Contact](actions/send-flow-to-contact.md) | POST | Sends a flow to a contact in Chatrace. |
| [Send Products To Contact](actions/send-products-to-contact.md) | POST | Sends products to a contact in Chatrace. |
| [Send Text Message To Contact](actions/send-text-message-to-contact.md) | POST | Sends a text message to a contact in Chatrace. |
| [Set Bot Field Value](actions/set-bot-field-value.md) | PUT | Updates a bot field value in Chatrace. |
| [Set Contact Custom Field](actions/set-contact-custom-field.md) | PUT | Updates a custom field on a Chatrace contact. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Account Admins](actions/list-account-admins.md) | GET | Retrieves account admins from your Chatrace account. |

