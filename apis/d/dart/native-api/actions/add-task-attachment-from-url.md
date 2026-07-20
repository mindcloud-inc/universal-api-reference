# Add Task Attachment From Url with Dart

Adds a URL attachment to a Dart task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:id/attachments/from-url`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [Add Task Attachment From Url](https://app.dartai.com/api/v0/public/docs/#/Attachment/addTaskAttachmentFromUrl)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `name` | body | `string` | no |
| `url` | body | `string` | no |
