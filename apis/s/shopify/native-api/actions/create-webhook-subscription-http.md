# Create Webhook Subscription (HTTP) with Shopify

Creates an HTTP webhook subscription in Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `2024-10/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [Create Webhook Subscription (HTTP)](https://shopify.dev/docs/api/admin-graphql/latest/mutations/webhookSubscriptionCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | — |
| `variables.webhookSubscription.callbackUrl` | body | `string` | yes | URL where the webhook subscription should send the POST request when the event occurs. |
| `variables` | body | `object` | no | — |
| `variables.topic` | body | `string` | yes | — |
| `variables.webhookSubscription.filter` | body | `string` | no | — |
| `variables.webhookSubscription.metafieldNamespaces` | body | `string` | no | Send multiple values as a array. |
| `variables.webhookSubscription` | body | `object` | no | — |
