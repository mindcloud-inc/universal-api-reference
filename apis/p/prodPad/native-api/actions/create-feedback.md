# Create Feedback with ProdPad

Creates new feedback in ProdPad.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedbacks`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Create Feedback](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PostFeedbacks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feedback` | body | `string` | yes |
| `contact_id` | body | `string` | no |
| `name` | body | `string` | no |
| `company_id` | body | `string` | no |
| `email` | body | `string` | no |
| `about` | body | `string` | no |
| `source` | body | `string` | no |
