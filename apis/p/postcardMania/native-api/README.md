# PostcardMania: Native API Reference

A consolidated summary of PostcardMania's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3
- **API base URL:** `https://v3.pcmintegrations.com`

## Authentication

### Bearer

Enter a single PostcardMania bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Favorite](actions/add-favorite.md) | `POST /gallery/favorites` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/puwo0pmljutyt) |
| [Add Suppressed Address](actions/add-suppressed-address.md) | `POST /suppression-list` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/gx39dwmmz7v0z) |
| [Bulk Cancel Orders](actions/bulk-cancel-orders.md) | `POST /order/bulk-cancel` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/gan0r8uot3zqe) |
| [Cancel Order](actions/cancel-order.md) | `DELETE /order/{{orderID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/iuc7kuzptpgwv) |
| [Create Access Token](actions/create-access-token.md) | `POST /auth/login` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/ffef03a112bb0) |
| [Create Carrier Route List Count](actions/create-carrier-route-list-count.md) | `POST /list/count/carrier-route` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/65o0jh0i3n7in-generating-a-list-count-by-carrier-route) |
| [Create Designer Design](actions/create-designer-design.md) | `POST /design/custom` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/76to9yvq9gav1) |
| [Create QR Code](actions/create-qr-code.md) | `POST /qr-code` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/bzxkzi7710kpf) |
| [Create Radius List Count](actions/create-radius-list-count.md) | `POST /list/count/radius` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/aafef87b8dd68-create-radius-list-count) |
| [Create Zipcode List Count](actions/create-zipcode-list-count.md) | `POST /list/count/zipcode` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/42360cfbf8ceb) |
| [Edit Designer Design](actions/edit-designer-design.md) | `GET /design/{{designID}}/edit` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/wys5o1p1fiq6g) |
| [Generate Brochure Design Proof](actions/generate-brochure-design-proof.md) | `POST /design/generate-proof/brochure` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/vhc4nw3yao2k5) |
| [Generate Greeting Card Design Proof](actions/generate-greeting-card-design-proof.md) | `POST /design/generate-proof/greeting-card` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/tvfmzffl7dxcr) |
| [Generate Letter Design Proof](actions/generate-letter-design-proof.md) | `POST /design/generate-proof/letter` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/mxy7r9t0zn812) |
| [Generate Postcard Design Proof](actions/generate-postcard-design-proof.md) | `POST /design/generate-proof/postcard` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/lbgea1ignycjv) |
| [Generate Recipient Proof](actions/generate-recipient-proof.md) | `POST /recipient/{{recipientId}}/generate-proof` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/b3ynzdasfi2mw) |
| [Generate Snap Apart Design Proof](actions/generate-snap-apart-design-proof.md) | `POST /design/generate-proof/snap-apart` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/q9blg22vnn4s2) |
| [Get Balances](actions/get-balances.md) | `GET /integration/balance` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/wb42dvrda7mdq) |
| [Get Batch](actions/get-batch.md) | `GET /batch/{{batchID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/b84f873587f9b) |
| [Get Batch Pricing](actions/get-batch-pricing.md) | `GET /batch/{{batchID}}/pricing` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3) |
| [Get Design](actions/get-design.md) | `GET /design/{{designID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/7fc283678ad23) |
| [Get Detailed Batch Mail Tracking](actions/get-detailed-batch-mail-tracking.md) | `GET /batch/{{batchID}}/mail-tracking-detailed` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3) |
| [Get Order](actions/get-order.md) | `GET /order/{{orderID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/70eb9283f87ef) |
| [Get Order Mail Tracking](actions/get-order-mail-tracking.md) | `GET /order/{{orderID}}/mail-tracking` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3) |
| [Get Order Pricing](actions/get-order-pricing.md) | `GET /order/{{orderID}}/pricing` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/92547af449aa8-direct-mail-api-v3) |
| [Get QR Code by Id](actions/get-qr-code-by-id.md) | `GET /qr-code/{{qrCodeID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/q1wjlwbbt9lrh) |
| [Get QR Code Tracking](actions/get-qr-code-tracking.md) | `GET /qr-code/{{qrCodeID}}/tracking` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/3u34crunm2sdh) |
| [List Batch Orders](actions/list-batch-orders.md) | `GET /batch/{{batchID}}/orders` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/uneg76q9gk3rh) |
| [List Batch Recipients](actions/list-batch-recipients.md) | `GET /batch/{{batchID}}/recipients` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/2cd98e3e8dc89) |
| [List Batches](actions/list-batches.md) | `GET /batch` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/2af7a5c1f97ee) |
| [List Demographic Options (Beta)](actions/list-demographic-options-beta.md) | `GET /list/demographics` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/9wms32o8hwei3-get-list-demographics-beta) |
| [List Design Tags](actions/list-design-tags.md) | `GET /gallery/tags/{{designID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/taolgqq6tv5wx) |
| [List Designs](actions/list-designs.md) | `GET /design` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/3d3a3000ff275) |
| [List Favorites](actions/list-favorites.md) | `GET /gallery/favorites` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/scurf2n9nkaly) |
| [List Gallery Designs](actions/list-gallery-designs.md) | `GET /gallery/designs` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/4l1p7s1ecfdzr) |
| [List Orders](actions/list-orders.md) | `GET /order` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/fdc898a0bcad2) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qr-code` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/od64yuiaubxz3) |
| [List Recipient List Types (Beta)](actions/list-recipient-list-types-beta.md) | `GET /list/types` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/455f0d2caecd4-get-list-types-beta) |
| [List Suppressed Addresses](actions/list-suppressed-addresses.md) | `GET /suppression-list` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/953lez0oqsza9) |
| [List Tags](actions/list-tags.md) | `GET /gallery/tags` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/sklugcm9gzn4q) |
| [List Undeliverable Recipients](actions/list-undeliverable-recipients.md) | `GET /recipient/undeliverable` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/wg1e1306pkidh) |
| [Place Brochure Order](actions/place-brochure-order.md) | `POST /order/brochure` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/0lk4yl0coc1e6) |
| [Place Brochure Order with List Count](actions/place-brochure-order-with-list-count.md) | `POST /order/brochure/with-list-count` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/ia3y208ptnvzr) |
| [Place Greeting Card Order](actions/place-greeting-card-order.md) | `POST /order/greeting-card` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/32c5b9fdoseh0) |
| [Place Greeting Card Order with List Count](actions/place-greeting-card-order-with-list-count.md) | `POST /order/greeting-card/with-list-count` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/vieoc2kdskeeh) |
| [Place Letter Order](actions/place-letter-order.md) | `POST /order/letter` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/130adee30e721) |
| [Place Letter Order with List Count](actions/place-letter-order-with-list-count.md) | `POST /order/letter/with-list-count` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/04960fa178488) |
| [Place Order using Webhook](actions/place-order-using-webhook.md) | `POST /order/webhook/{{webhookID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/393aq3ihkf5ec) |
| [Place Postcard Order](actions/place-postcard-order.md) | `POST /order/postcard` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/24b58db675dad) |
| [Place Postcard Order with List Count](actions/place-postcard-order-with-list-count.md) | `POST /order/postcard/with-list-count` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/f9c7a78b2bb20) |
| [Place Snap-Apart Order](actions/place-snap-apart-order.md) | `POST /order/snap-apart` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/xclc333y2rd0a) |
| [Place Snap-Apart Order with List Count](actions/place-snap-apart-order-with-list-count.md) | `POST /order/snap-apart/with-list-count` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/352wuxnk4nib3) |
| [Remove Design](actions/remove-design.md) | `DELETE /design/{{designID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/cy77m4nleab57) |
| [Remove Favorite](actions/remove-favorite.md) | `DELETE /gallery/favorites` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/ftr8buwowrb01) |
| [Remove Suppressed Address](actions/remove-suppressed-address.md) | `DELETE /suppression-list/{{suppressionAddressID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/vp81vl1e1rq3t) |
| [Rename Design](actions/rename-design.md) | `PUT /design/{{designID}}` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/3eg5izp9nvj8m) |
| [Verify Recipients](actions/verify-recipients.md) | `POST /recipient/verify` | [docs](https://docs.pcmintegrations.com/docs/directmail-api/k49y925eo4waw) |
