# Create Template with Superchat

Creates a new template in Superchat.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Create Template](https://developers.superchat.com/reference/createatemplate-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Internal name of the template |
| `folder_id` | body | `string` | no | The ID of the folder this template should be save in. |
| `content` | body | `object` | no | — |
| `whats_app_business_account_id` | body | `string` | no | The WhatsApp business account on which the template should be created. Required for WhatsApp templates. Starts with `waba_` Get the ID from the /channels or /channels/{channel_id} endpoint. |
