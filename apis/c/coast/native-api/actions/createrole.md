# Create Role with Coast

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/roles`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Create Role](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the role |
| `description` | body | `string` | yes | Description of the role |
| `permissions` | body | `object` | yes | Role permissions object |
