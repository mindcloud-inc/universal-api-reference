# Revoke organization API key with Neon

Revokes a organization API key from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:org_id/api_keys/:key_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Revoke organization API key](https://api-docs.neon.tech/reference/revokeorgapikey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `key_id` | path | `number` | yes | Neon API parameter key_id |
