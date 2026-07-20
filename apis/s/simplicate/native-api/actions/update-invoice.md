# Update Invoice with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/invoice/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Invoice](https://developer.simplicate.com/docs/api/v2/reference/update-invoices-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comments` | body | `string` | no | Invoice comments. |
| `date` | body | `string` | no | Invoice date in YYYY-MM-DD format. |
| `id` | path | `string` | yes | Invoice identifier. |
| `my_organization_profile_id` | body | `string` | no | My organization profile identifier. |
| `organization_id` | body | `string` | no | Invoice recipient organization identifier. |
| `project_id` | body | `string` | no | Related project identifier. |
| `reference` | body | `string` | no | Invoice reference. |
| `subject` | body | `string` | no | Invoice subject. |
