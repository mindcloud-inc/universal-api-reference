# List Feedback with ProdPad

Retrieves feedback from ProdPad.

## Endpoint

- **Method:** `GET`
- **Path:** `/feedbacks`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [List Feedback](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetFeedbacks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_by` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `company` | query | `string` | no | — |
| `customer` | query | `string` | no | — |
| `product` | query | `string` | no | — |
| `persona` | query | `string` | no | — |
| `job_role` | query | `string` | no | — |
| `tags` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `has_ideas` | query | `boolean` | no | — |
| `external_id` | query | `string` | no | — |
| `external_url` | query | `string` | no | — |
