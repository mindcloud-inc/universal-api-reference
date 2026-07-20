# Create Sale with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/sales/sales`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Sale](https://developer.simplicate.com/docs/api/v2/reference/create-sales-sales/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `my_organization_profile_id` | body | `string` | no | The organization profile id for the sale |
| `note` | body | `string` | no | A note for the sale |
| `organization_id` | body | `string` | no | The organization id for the sale |
| `progress_id` | body | `string` | no | The sale progress id |
| `status_id` | body | `string` | no | The sale status id |
| `subject` | body | `string` | no | The sale subject |
