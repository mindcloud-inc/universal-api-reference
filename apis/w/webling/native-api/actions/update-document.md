# Update Document with Webling

## Endpoint

- **Method:** `PUT`
- **Path:** `/document/:id`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [Update Document](https://demo.webling.ch/api/1#document-document-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Document ID to update. |
| `properties.title` | body | `string` | yes | Document title. |
| `parents` | body | `number` | yes | Parent document group ID. |
