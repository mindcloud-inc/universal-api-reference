# Create Signature Request with Yousign

Creates a new signature request in Yousign.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Create Signature Request](https://developers.yousign.com/reference/post-signature_requests-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Signature request name. |
| `delivery_mode` | body | `string` | yes | How Yousign should notify signers: email or none. |
| `ordered_signers` | body | `boolean` | no | Whether signers should be processed sequentially. |
| `workspace_id` | body | `string` | no | Workspace ID to scope the signature request. |
| `timezone` | body | `string` | no | Signature request timezone. |
| `expiration_date` | body | `string` | no | Due date in yyyy-mm-dd format. |
| `external_id` | body | `string` | no | External identifier to attach to the signature request. |
| `template_id` | body | `string` | no | Existing Yousign template ID to base the signature request on. |
| `signers_allowed_to_decline` | body | `boolean` | no | Whether signers may decline to sign. |
