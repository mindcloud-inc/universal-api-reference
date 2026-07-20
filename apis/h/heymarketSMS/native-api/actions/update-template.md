# Update Template with Heymarket SMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/template/:id`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Update Template](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the template. |
| `title` | body | `string` | yes | Template name. |
| `content.text` | body | `string` | yes | Text content for the template body. |
| `archived` | body | `boolean` | no | Whether the template should be archived. |
| `local_id` | body | `string` | no | Client unique identifier for the template. |
