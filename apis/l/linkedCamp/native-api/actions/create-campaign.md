# Create Campaign with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Create Campaign](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Campaign title. |
| `url` | body | `string` | no | Optional URL associated with the campaign. |
| `sequence` | body | `string` | yes | Campaign sequence type, such as CONNECT, MESSAGE, INMAIL, or EMAIL. |
| `content` | body | `object` | yes | Campaign content object matching the selected sequence type. |
