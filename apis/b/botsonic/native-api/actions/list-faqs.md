# List FAQs with Botsonic

Retrieves all FAQs from a Botsonic bot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot-faq/all`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [List FAQs](https://docs.botsonic.com/reference/get_all_faqs_v1_business_bot_faq_all_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Search for FAQs matching a query. |
| `sort_by` | query | `string` | no | FAQ attribute to sort by. |
| `sort_order` | query | `string` | no | Sort direction for FAQ results. |
