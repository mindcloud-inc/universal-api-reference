# Woodpecker.co: Get Inbox Messages

Retrieves inbox messages from the Woodpecker inbox.

```
GET https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-inbox-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-inbox-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-inbox-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignIds` | string<number> | no | Filter inbox messages by campaign IDs. Accepts multiple values in one string, delimited by `,`. |
| `mailboxIds` | string<number> | no | Filter inbox messages by mailbox IDs. Accepts multiple values in one string, delimited by `,`. |
| `nextPageCursor` | string | no | Cursor for the next inbox page. |
| `outOfCampaign` | string | no | Filter inbox messages to those outside campaigns. |
| `perPage` | number | no | Number of inbox messages per page. |
| `previousPageCursor` | string | no | Cursor for the previous inbox page. |
| `prospectInterestLevel` | string | no | Filter inbox messages by prospect interest level. |
| `prospectStatus` | string | no | Filter inbox messages by prospect status. |
| `read` | boolean | no | Filter inbox messages by read status. |
| `searchPhrases` | string<string> | no | Filter inbox messages by search phrases. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `GET /rest/v2/inbox/messages` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-messages.md) for the provider-specific parameters and requirements.

