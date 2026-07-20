# Update Contact with ProdPad

Updates an existing contact in ProdPad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Update Contact](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PutContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | — |
| `about` | body | `string` | no | Details about the contact. |
| `phone` | body | `string` | no | Phone number of the contact. |
| `twitter_url` | body | `string` | no | Twitter handle or URL for the contact. |
| `company` | body | `string` | no | UUID of the company to link to the contact. |
| `job_role` | body | `string` | no | UUID of the job role. |
