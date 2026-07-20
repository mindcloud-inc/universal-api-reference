# Update Rule with Vouchery.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/rules/:id`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Update Rule](https://docs.vouchery.io/reference/putapiv21rulesid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Rule ID from Vouchery. |
| `operator` | body | `string` | yes | Rule operator. |
| `type` | body | `string` | yes | Rule type discriminator for update. |
| `value` | body | `number` | yes | Rule value. |
