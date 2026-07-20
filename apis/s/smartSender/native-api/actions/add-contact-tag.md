# Add Contact Tag with Smart Sender

Adds a tag to a contact in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/:contactId/tags/:tagId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Add Contact Tag](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97386531/Contact%2BTags%2BAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
| `tagId` | path | `string` | yes | The Smart Sender tag ID. |
