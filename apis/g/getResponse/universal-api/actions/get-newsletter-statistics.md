# GetResponse: Get Newsletter Statistics

Retrieves total newsletter statistics from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-newsletter-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-newsletter-statistics?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-newsletter-statistics?${params}`, {
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
| `campaignId` | string | no | Campaign identifier for statistics lookup |
| `newsletterId` | string | no | Newsletter identifier for statistics lookup |
| `groupBy` | string | no | Group newsletter statistics by interval |
| `createdOnFrom` | string | no | Start date for statistics window |
| `createdOnTo` | string | no | End date for statistics window |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sent": 1,
      "timeInterval": "string",
      "totalClicked": 1,
      "totalOpened": 1,
      "unsubscribed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sent` | number |  |
| `timeInterval` | string |  |
| `totalClicked` | number |  |
| `totalOpened` | number |  |
| `unsubscribed` | number |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /newsletters/statistics` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-newsletter-statistics.md) for the provider-specific parameters and requirements.

