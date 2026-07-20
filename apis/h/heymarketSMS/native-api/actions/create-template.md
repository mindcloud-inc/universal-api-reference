# Create Template with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/template`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Create Template](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Template name. |
| `content.text` | body | `string` | yes | Text content for the template body. |
| `archived` | body | `boolean` | no | Whether the template should be archived. |
| `local_id` | body | `string` | no | Client unique identifier for the template. |
