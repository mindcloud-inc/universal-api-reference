# Send Item To Inbox with Dynalist

Creates a new inbox item in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/add`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Send Item To Inbox](https://apidocs.dynalist.io/#send-to-inbox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | body | `number` | no | Inbox insertion index; use -1 for the end. |
| `content` | body | `string` | no | Inbox item content. |
| `note` | body | `string` | no | Optional inbox item note. |
| `checked` | body | `boolean` | no | Whether the inbox item is checked. |
| `checkbox` | body | `boolean` | no | Whether the inbox item has a checkbox. |
| `heading` | body | `number` | no | Heading level. |
| `color` | body | `number` | no | Dynalist color index. |
