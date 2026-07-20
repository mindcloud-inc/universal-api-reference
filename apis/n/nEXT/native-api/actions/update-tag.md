# Update Tag with NEXT

Updates an existing tag in NEXT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:id`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Update Tag](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The NEXT tag ID. |
| `name` | body | `string` | yes | Updated tag name. |
