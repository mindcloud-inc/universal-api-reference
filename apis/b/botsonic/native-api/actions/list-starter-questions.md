# List Starter Questions with Botsonic

Retrieves all starter questions from Botsonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot-starter-questions/all`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [List Starter Questions](https://docs.botsonic.com/reference/get_all_starter_questions_v1_business_bot_starter_questions_all_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Optional search query. |
| `sort_by` | query | `string` | no | Starter-question field to sort by. |
| `sort_order` | query | `string` | no | Sort direction. |
