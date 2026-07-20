# GMass: List Campaign Replies

Retrieves recipients who replied to a GMass campaign.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-replies?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-replies?${params}`, {
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
| `campaignId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alreadyReplied": true,
      "emailAddress": "ava@example.com",
      "replyId": 1,
      "replyTime": "2026-05-07T12:00:00.000Z",
      "sender": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alreadyReplied` | boolean |  |
| `emailAddress` | string |  |
| `replyId` | number |  |
| `replyTime` | date |  |
| `sender` | string |  |

## Native endpoint

Through the native GMass API, this operation is `GET /reports/:campaignId/replies` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-replies.md) for the provider-specific parameters and requirements.

