# Update AI Rule with NEXT

Updates an existing AI rule in NEXT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ai-rules/:id`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Update AI Rule](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The AI rule ID. |
| `name` | body | `string` | yes | Updated AI rule name. |
| `status` | body | `string` | yes | Updated AI rule status. |
| `data` | body | `string` | yes | Updated AI rule definition payload. |
| `type` | body | `string` | yes | Updated AI rule type. |
