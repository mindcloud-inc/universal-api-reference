# Create Contact with ProdPad

Creates a new contact in ProdPad.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Create Contact](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PostContacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `email` | body | `string` | yes |
| `about` | body | `string` | no |
| `phone` | body | `string` | no |
| `twitter_url` | body | `string` | no |
| `company` | body | `string` | no |
| `job_role` | body | `string` | no |
