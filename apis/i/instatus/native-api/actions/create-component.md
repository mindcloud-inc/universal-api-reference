# Create Component with Instatus

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:page_id/components`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Create Component](https://instatus.com/help/api/components)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Component description. |
| `name` | body | `string` | no | Component name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `status` | body | `string` | no | Component status, such as OPERATIONAL or PARTIALOUTAGE. |
