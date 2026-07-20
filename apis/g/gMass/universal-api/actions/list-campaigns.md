# GMass: List Campaigns

Retrieves GMass campaigns and their aggregate statistics.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaigns?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "creationTime": "2026-05-07T12:00:00.000Z",
      "friendlyName": "Ava Chen",
      "fromLine": "string",
      "stage": 1,
      "statistics": {
        "blocks": 1,
        "bounces": 1,
        "clicks": 1,
        "opens": 1,
        "recipients": 1,
        "replies": 1,
        "unsubscribes": 1
      },
      "status": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `creationTime` | date |  |
| `friendlyName` | string |  |
| `fromLine` | string |  |
| `stage` | number |  |
| `statistics.blocks` | number |  |
| `statistics.bounces` | number |  |
| `statistics.clicks` | number |  |
| `statistics.opens` | number |  |
| `statistics.recipients` | number |  |
| `statistics.replies` | number |  |
| `statistics.unsubscribes` | number |  |
| `status` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native GMass API, this operation is `GET /campaigns` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

