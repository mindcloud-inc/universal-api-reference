# Create organization API key with Neon

Creates a organization API key in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:org_id/api_keys`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create organization API key](https://api-docs.neon.tech/reference/createorgapikey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `key_name` | body | `string` | yes | Neon API parameter key_name |
| `project_id` | body | `string` | no | Neon API parameter project_id |
