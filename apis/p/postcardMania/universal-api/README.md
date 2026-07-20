# <img src="https://images.mindcloud.co/apps/icons/4159fb04-7a5f-499f-9df1-95b3fe352b86_1774468439005.jpeg" alt="PostcardMania logo" width="28" height="28"> PostcardMania: Universal API

PostcardMania DirectMail API integration for automating postcard and direct mail workflows from MindCloud. The provider positions the API as a direct-mail automation surface for managing recipient lists, designs, orders, batches, and related mailing operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postcardMania/latest
- **Category:** Marketing
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pcmintegrations.com/direct-mail-api/
- **Vendor API docs:** https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Edit Designer Design](actions/edit-designer-design.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/edit-designer-design?connectionId=$CONNECTION_ID&designID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | POST | Creates a new access token in PostcardMania. |

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Add Suppressed Address](actions/add-suppressed-address.md) | POST | Creates a new suppressed address in PostcardMania. |
| [List Suppressed Addresses](actions/list-suppressed-addresses.md) | GET | Retrieves suppressed addresses from PostcardMania. |
| [Remove Suppressed Address](actions/remove-suppressed-address.md) | DELETE | Deletes an existing suppressed address from PostcardMania. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch from PostcardMania. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches from PostcardMania. |

### Design

| Action | Method | Description |
| --- | --- | --- |
| [Get Design](actions/get-design.md) | GET | Retrieves a design from PostcardMania. |
| [List Designs](actions/list-designs.md) | GET | Retrieves designs from PostcardMania. |
| [Remove Design](actions/remove-design.md) | DELETE | Deletes an existing design from PostcardMania. |
| [Rename Design](actions/rename-design.md) | PUT | Updates an existing design in PostcardMania. |

### List Count

| Action | Method | Description |
| --- | --- | --- |
| [Create Carrier Route List Count](actions/create-carrier-route-list-count.md) | POST | Creates a carrier route list count in PostcardMania. |
| [Create Radius List Count](actions/create-radius-list-count.md) | POST | Creates a radius list count in PostcardMania. |
| [Create Zipcode List Count](actions/create-zipcode-list-count.md) | POST | Creates a ZIP code list count in PostcardMania. |

### List Demographic

| Action | Method | Description |
| --- | --- | --- |
| [List Demographic Options (Beta)](actions/list-demographic-options-beta.md) | GET | Retrieves beta demographic options from PostcardMania. |

### List Type

| Action | Method | Description |
| --- | --- | --- |
| [List Recipient List Types (Beta)](actions/list-recipient-list-types-beta.md) | GET | Retrieves beta recipient list types from PostcardMania. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | DELETE | Cancels an existing order in PostcardMania. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from PostcardMania. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from PostcardMania. |
| [Place Letter Order](actions/place-letter-order.md) | POST | Creates a new letter order in PostcardMania. |
| [Place Postcard Order](actions/place-postcard-order.md) | POST | Creates a new postcard order in PostcardMania. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Cancel Orders](actions/bulk-cancel-orders.md) | DELETE | Cancels existing orders in PostcardMania in bulk. |
| [Get Order Mail Tracking](actions/get-order-mail-tracking.md) | GET | Retrieves mail tracking for a PostcardMania order. |
| [Get Order Pricing](actions/get-order-pricing.md) | GET | Retrieves pricing for a PostcardMania order. |
| [List Batch Orders](actions/list-batch-orders.md) | GET | Retrieves orders from a PostcardMania batch. |
| [Place Brochure Order](actions/place-brochure-order.md) | POST | Creates a new brochure order in PostcardMania. |
| [Place Brochure Order with List Count](actions/place-brochure-order-with-list-count.md) | POST | Creates a brochure order from a list count in PostcardMania. |
| [Place Greeting Card Order](actions/place-greeting-card-order.md) | POST | Creates a new greeting card order in PostcardMania. |
| [Place Greeting Card Order with List Count](actions/place-greeting-card-order-with-list-count.md) | POST | Creates a greeting card order from a list count in PostcardMania. |
| [Place Letter Order with List Count](actions/place-letter-order-with-list-count.md) | POST | Creates a letter order from a list count in PostcardMania. |
| [Place Order using Webhook](actions/place-order-using-webhook.md) | POST | Creates a new order in PostcardMania using a webhook. |
| [Place Postcard Order with List Count](actions/place-postcard-order-with-list-count.md) | POST | Creates a postcard order from a list count in PostcardMania. |
| [Place Snap-Apart Order](actions/place-snap-apart-order.md) | POST | Creates a new snap-apart order in PostcardMania. |
| [Place Snap-Apart Order with List Count](actions/place-snap-apart-order-with-list-count.md) | POST | Creates a snap-apart order from a list count in PostcardMania. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a new QR code in PostcardMania. |
| [Generate Recipient Proof](actions/generate-recipient-proof.md) | POST | Creates a proof for a PostcardMania recipient. |
| [Get Balances](actions/get-balances.md) | GET | Retrieves account balances from PostcardMania. |
| [Get Batch Pricing](actions/get-batch-pricing.md) | GET | Retrieves pricing for a PostcardMania batch. |
| [Get Detailed Batch Mail Tracking](actions/get-detailed-batch-mail-tracking.md) | GET | Retrieves detailed mail tracking for a PostcardMania batch. |
| [Get QR Code by Id](actions/get-qr-code-by-id.md) | GET | Retrieves a QR code from PostcardMania. |
| [Get QR Code Tracking](actions/get-qr-code-tracking.md) | GET | Retrieves tracking for a PostcardMania QR code. |
| [List Batch Recipients](actions/list-batch-recipients.md) | GET | Retrieves recipients from a PostcardMania batch. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from PostcardMania. |
| [List Undeliverable Recipients](actions/list-undeliverable-recipients.md) | GET | Retrieves undeliverable recipients from PostcardMania. |
| [Verify Recipients](actions/verify-recipients.md) | POST | Verifies mailing recipients in PostcardMania. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Add Favorite](actions/add-favorite.md) | POST | Creates a new favorite design in PostcardMania. |
| [Create Designer Design](actions/create-designer-design.md) | POST | Creates a new designer design in PostcardMania. |
| [Edit Designer Design](actions/edit-designer-design.md) | GET | Retrieves an edit session for a PostcardMania design. |
| [Generate Brochure Design Proof](actions/generate-brochure-design-proof.md) | POST | Creates a brochure design proof in PostcardMania. |
| [Generate Greeting Card Design Proof](actions/generate-greeting-card-design-proof.md) | POST | Creates a greeting card design proof in PostcardMania. |
| [Generate Letter Design Proof](actions/generate-letter-design-proof.md) | POST | Creates a letter design proof in PostcardMania. |
| [Generate Postcard Design Proof](actions/generate-postcard-design-proof.md) | POST | Creates a postcard design proof in PostcardMania. |
| [Generate Snap Apart Design Proof](actions/generate-snap-apart-design-proof.md) | POST | Creates a snap-apart design proof in PostcardMania. |
| [List Design Tags](actions/list-design-tags.md) | GET | Retrieves tags for a PostcardMania design. |
| [List Favorites](actions/list-favorites.md) | GET | Retrieves favorite designs from PostcardMania. |
| [List Gallery Designs](actions/list-gallery-designs.md) | GET | Retrieves gallery designs from PostcardMania. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from PostcardMania. |
| [Remove Favorite](actions/remove-favorite.md) | DELETE | Deletes an existing favorite from PostcardMania. |

