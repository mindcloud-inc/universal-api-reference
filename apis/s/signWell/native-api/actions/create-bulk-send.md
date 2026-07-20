# Create Bulk Send with SignWell

Creates a new bulk send in SignWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk_sends`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Create Bulk Send](https://developers.signwell.com/reference/post_api-v1-bulk-sends)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_ids[]` | body | `array<string>` | yes | Unique identifiers for a list of templates. |
| `bulk_send_csv` | body | `string` | yes | A RFC 4648 base64 string of the template CSV file to be validated. |
| `skip_row_errors` | body | `boolean` | no | Whether to skip errors in the rows. Defaults to false. |
| `api_application_id` | body | `string` | no | Unique identifier for API Application settings to use. |
| `name` | body | `string` | no | The name of the Bulk Send. |
| `subject` | body | `string` | no | Email subject for the signature request that recipients will see. |
| `message` | body | `string` | no | Email message for the signature request that recipients will see. |
| `apply_signing_order` | body | `boolean` | no | When true recipients will sign one at a time in the documented order. |
| `custom_requester_name` | body | `string` | no | Sets the custom requester name for the document. |
| `custom_requester_email` | body | `string` | no | Sets the custom requester email for the document. |
