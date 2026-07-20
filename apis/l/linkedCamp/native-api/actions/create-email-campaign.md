# Create Email Campaign with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Create Email Campaign](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Campaign title. |
| `content.subject1` | body | `string` | yes | First email subject. |
| `content.content1` | body | `string` | yes | First email message. |
| `content.subject2` | body | `string` | no | Optional second email subject. |
| `content.content2` | body | `string` | no | Optional second email message. |
| `content.subject3` | body | `string` | no | Optional third email subject. |
| `content.content3` | body | `string` | no | Optional third email message. |
