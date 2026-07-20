# Chatrace: Native API Reference

A consolidated summary of Chatrace's API configuration and 55 documented operations, with links to official documentation.

- **Official docs:** https://docs.chatrace.com/kb/chatrace-api-documentation/
- **OpenAPI specification:** https://api.chatrace.com/swagger/swagger.json?v=15
- **API base URL:** `https://api.chatrace.com`

## Authentication

### API Key

Use the Chatrace API access token. Runtime requests send the token in the X-ACCESS-TOKEN header.

### Credentials

- **API Key:** `apiKey` · optional · The Chatrace access token sent in the X-ACCESS-TOKEN request header.

Send these headers with each API request:

```http
X-ACCESS-TOKEN: <apiKey>
```

[Official authentication documentation](https://docs.chatrace.com/kb/chatrace-api-documentation/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (55 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Product To Cart](actions/add-product-to-cart.md) | `POST /contacts/:contact_id/cart/:product_id` | [docs](https://api.chatrace.com/swagger/) |
| [Add Tag To Contact](actions/add-tag-to-contact.md) | `POST /contacts/:contact_id/tags/:tag_id` | [docs](https://api.chatrace.com/swagger/) |
| [Clear Contact Cart](actions/clear-contact-cart.md) | `DELETE /contacts/:contact_id/cart` | [docs](https://api.chatrace.com/swagger/) |
| [Create Account Custom Field](actions/create-account-custom-field.md) | `POST /accounts/custom_fields` | [docs](https://api.chatrace.com/swagger/) |
| [Create Account Tag](actions/create-account-tag.md) | `POST /accounts/tags` | [docs](https://api.chatrace.com/swagger/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.chatrace.com/swagger/) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /pipelines/:pipeline_id/opportunities` | [docs](https://api.chatrace.com/swagger/) |
| [Create Opportunity Comment](actions/create-opportunity-comment.md) | `POST /pipelines/:pipeline_id/opportunities/:opportunity_id/comments` | [docs](https://api.chatrace.com/swagger/) |
| [Delete Account Tag](actions/delete-account-tag.md) | `DELETE /accounts/tags/:tag_id` | [docs](https://api.chatrace.com/swagger/) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE /pipelines/:pipeline_id/opportunities/:opportunity_id` | [docs](https://api.chatrace.com/swagger/) |
| [Delete Opportunity Comment](actions/delete-opportunity-comment.md) | `DELETE /pipelines/:pipeline_id/opportunities/:opportunity_id/comments/:comment_id` | [docs](https://api.chatrace.com/swagger/) |
| [Find Contacts By Custom Field](actions/find-contacts-by-custom-field.md) | `GET /contacts/find_by_custom_field` | [docs](https://api.chatrace.com/swagger/) |
| [Generate Template Link](actions/generate-template-link.md) | `POST /accounts/template/:template_id/generateSingleUseLink` | [docs](https://api.chatrace.com/swagger/) |
| [Get Account Custom Field](actions/get-account-custom-field.md) | `GET /accounts/custom_fields/:custom_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Account Custom Field By Name](actions/get-account-custom-field-by-name.md) | `GET /accounts/custom_fields/name/:custom_field_name` | [docs](https://api.chatrace.com/swagger/) |
| [Get Account Integrations](actions/get-account-integrations.md) | `GET /accounts/integrations` | [docs](https://api.chatrace.com/swagger/) |
| [Get Account Tag](actions/get-account-tag.md) | `GET /accounts/tags/:tag_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Account Tag By Name](actions/get-account-tag-by-name.md) | `GET /accounts/tags/name/:tag_name` | [docs](https://api.chatrace.com/swagger/) |
| [Get Bot Field Value](actions/get-bot-field-value.md) | `GET /accounts/bot_fields/:bot_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendars/:calendar_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Contact Cart](actions/get-contact-cart.md) | `GET /contacts/:contact_id/cart` | [docs](https://api.chatrace.com/swagger/) |
| [Get Contact Custom Field](actions/get-contact-custom-field.md) | `GET /contacts/:contact_id/custom_fields/:custom_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Contact Order](actions/get-contact-order.md) | `GET /contacts/:contact_id/order/:order_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /pipelines/:pipeline_id/opportunities/:opportunity_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /pipelines/:pipeline_id` | [docs](https://api.chatrace.com/swagger/) |
| [Get Product](actions/get-product.md) | `GET /products/:product_id` | [docs](https://api.chatrace.com/swagger/) |
| [List Account Admins](actions/list-account-admins.md) | `GET /accounts/admins` | [docs](https://api.chatrace.com/swagger/) |
| [List Account Custom Fields](actions/list-account-custom-fields.md) | `GET /accounts/custom_fields` | [docs](https://api.chatrace.com/swagger/) |
| [List Account Flows](actions/list-account-flows.md) | `GET /accounts/flows` | [docs](https://api.chatrace.com/swagger/) |
| [List Account Tags](actions/list-account-tags.md) | `GET /accounts/tags` | [docs](https://api.chatrace.com/swagger/) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars/` | [docs](https://api.chatrace.com/swagger/) |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | `GET /contacts/:contact_id/custom_fields` | [docs](https://api.chatrace.com/swagger/) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /contacts/:contact_id/tags` | [docs](https://api.chatrace.com/swagger/) |
| [List Opportunities](actions/list-opportunities.md) | `GET /pipelines/:pipeline_id/opportunities` | [docs](https://api.chatrace.com/swagger/) |
| [List Opportunity Comments](actions/list-opportunity-comments.md) | `GET /pipelines/:pipeline_id/opportunities/:opportunity_id/comments` | [docs](https://api.chatrace.com/swagger/) |
| [List Pipeline Custom Fields](actions/list-pipeline-custom-fields.md) | `GET /pipelines/:pipeline_id/custom_fields` | [docs](https://api.chatrace.com/swagger/) |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | `GET /pipelines/:pipeline_id/stages` | [docs](https://api.chatrace.com/swagger/) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines/` | [docs](https://api.chatrace.com/swagger/) |
| [Mark Order As Paid](actions/mark-order-as-paid.md) | `POST /contacts/:contact_id/pay/:order_id` | [docs](https://api.chatrace.com/swagger/) |
| [Remove Bot Field Value](actions/remove-bot-field-value.md) | `DELETE /accounts/bot_fields/:bot_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Remove Contact Custom Field](actions/remove-contact-custom-field.md) | `DELETE /contacts/:contact_id/custom_fields/:custom_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Remove Product From Cart](actions/remove-product-from-cart.md) | `DELETE /contacts/:contact_id/cart/:product_id` | [docs](https://api.chatrace.com/swagger/) |
| [Remove Tag From Contact](actions/remove-tag-from-contact.md) | `DELETE /contacts/:contact_id/tags/:tag_id` | [docs](https://api.chatrace.com/swagger/) |
| [Send Content To Contact](actions/send-content-to-contact.md) | `POST /contacts/:contact_id/send_content` | [docs](https://api.chatrace.com/swagger/) |
| [Send File To Contact](actions/send-file-to-contact.md) | `POST /contacts/:contact_id/send/file` | [docs](https://api.chatrace.com/swagger/) |
| [Send Flow To Contact](actions/send-flow-to-contact.md) | `POST /contacts/:contact_id/send/:flow_id` | [docs](https://api.chatrace.com/swagger/) |
| [Send Products To Contact](actions/send-products-to-contact.md) | `POST /contacts/:contact_id/send/products` | [docs](https://api.chatrace.com/swagger/) |
| [Send Text Message To Contact](actions/send-text-message-to-contact.md) | `POST /contacts/:contact_id/send/text` | [docs](https://api.chatrace.com/swagger/) |
| [Set Bot Field Value](actions/set-bot-field-value.md) | `POST /accounts/bot_fields/:bot_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Set Contact Custom Field](actions/set-contact-custom-field.md) | `POST /contacts/:contact_id/custom_fields/:custom_field_id` | [docs](https://api.chatrace.com/swagger/) |
| [Transfer Opportunity To Pipeline](actions/transfer-opportunity-to-pipeline.md) | `POST /pipelines/:pipeline_id/opportunities/:opportunity_id/transfer-to-pipeline` | [docs](https://api.chatrace.com/swagger/) |
| [Update Contact Order](actions/update-contact-order.md) | `POST /contacts/:contact_id/order/:order_id` | [docs](https://api.chatrace.com/swagger/) |
| [Update Opportunity](actions/update-opportunity.md) | `POST /pipelines/:pipeline_id/opportunities/:opportunity_id` | [docs](https://api.chatrace.com/swagger/) |
| [Update Product](actions/update-product.md) | `POST /products/:product_id` | [docs](https://api.chatrace.com/swagger/) |
