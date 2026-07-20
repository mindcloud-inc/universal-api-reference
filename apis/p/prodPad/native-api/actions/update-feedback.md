# Update Feedback with ProdPad

Updates existing feedback in ProdPad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/feedbacks/:id`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Update Feedback](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PutFeedback)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `feedback` | body | `string` | no |
| `state` | body | `string` | no |
