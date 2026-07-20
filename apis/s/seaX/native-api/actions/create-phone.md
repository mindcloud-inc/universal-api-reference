# Create Phone with SeaX

Creates a phone number in the current SeaX workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/phones`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Create Phone](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled_dnc_reply` | body | `boolean` | yes | Whether DNC reply is enabled. |
| `enabled_generic_reply` | body | `boolean` | yes | Whether generic reply is enabled. |
| `name` | body | `string` | yes | Phone display name. |
| `phone` | body | `string` | yes | Phone number. |
| `source` | body | `object` | yes | Phone source. |
| `type` | body | `object` | yes | Phone type. |
