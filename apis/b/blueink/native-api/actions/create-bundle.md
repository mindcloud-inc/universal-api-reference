# Create Bundle with Blueink

Creates a new bundle in Blueink.

## Endpoint

- **Method:** `POST`
- **Path:** `/bundles/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Create Bundle](https://developer.blueink.com/api/#tag/Bundles/operation/createBundle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_test` | body | `boolean` | no | Create the bundle as a test bundle. |
| `status` | body | `string` | no | Use dr to create a draft bundle without sending it. |
| `packets[].key` | body | `string` | yes | Unique signer key for the bundle. |
| `packets[].name` | body | `string` | yes | Name of the signer. |
| `packets[].email` | body | `string` | yes | Email address of the signer. |
| `documents[].template_id` | body | `string` | yes | Document template ID to include in the bundle. |
| `documents[].assignments[].role` | body | `string` | yes | Template role to assign. |
| `documents[].assignments[].signer` | body | `string` | yes | Signer key to bind to the template role. |
