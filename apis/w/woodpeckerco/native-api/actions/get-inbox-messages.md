# Get Inbox Messages with Woodpecker.co

Retrieves inbox messages from the Woodpecker inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/inbox/messages`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Get Inbox Messages](https://developers.woodpecker.co/docs/inbox/get-inbox-messages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_ids` | query | `string<number>` | no | Filter inbox messages by campaign IDs. Send multiple values as a string separated by `,`. |
| `mailbox_ids` | query | `string<number>` | no | Filter inbox messages by mailbox IDs. Send multiple values as a string separated by `,`. |
| `next_page_cursor` | query | `string` | no | Cursor for the next inbox page. |
| `out_of_campaign` | query | `string` | no | Filter inbox messages to those outside campaigns. |
| `per_page` | query | `number` | no | Number of inbox messages per page. |
| `previous_page_cursor` | query | `string` | no | Cursor for the previous inbox page. |
| `prospect_interest_level` | query | `string` | no | Filter inbox messages by prospect interest level. |
| `prospect_status` | query | `string` | no | Filter inbox messages by prospect status. |
| `read` | query | `boolean` | no | Filter inbox messages by read status. |
| `search_phrases` | query | `string<string>` | no | Filter inbox messages by search phrases. Send multiple values as a string separated by `,`. |
