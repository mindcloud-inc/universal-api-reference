# Create InMail Campaign with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Create InMail Campaign](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Campaign title. |
| `url` | body | `string` | no | Optional LinkedIn search URL used as the campaign source. |
| `content.subject1` | body | `string` | yes | First InMail subject. |
| `content.content1` | body | `string` | yes | First InMail message. |
| `content.subject2` | body | `string` | no | Optional second InMail subject. |
| `content.content2` | body | `string` | no | Optional second InMail message. |
| `content.subject3` | body | `string` | no | Optional third InMail subject. |
| `content.content3` | body | `string` | no | Optional third InMail message. |
