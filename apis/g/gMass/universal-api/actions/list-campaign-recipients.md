# GMass: List Campaign Recipients

Retrieves recipients from a GMass campaign.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-recipients?${params}`, {
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
| `stage` | number | no |  |
| `date` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddress": "ava@example.com",
      "gmailResponseText": "string",
      "sender": "string",
      "sentTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string |  |
| `gmailResponseText` | string |  |
| `sender` | string |  |
| `sentTime` | date |  |

## Native endpoint

Through the native GMass API, this operation is `GET /reports/:campaignId/recipients` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-recipients.md) for the provider-specific parameters and requirements.

