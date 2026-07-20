# Socket: Get Repository Analytics

Retrieves repository analytics data from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-repository-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-repository-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-repository-analytics?${params}`, {
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
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].createdAt` | string |  |
| `items[].id` | number |  |
| `items[].organizationId` | number |  |
| `items[].repositoryId` | string |  |
| `items[].repositoryName` | string |  |
| `items[].topFiveAlertTypes` | object |  |
| `items[].totalCriticalAdded` | number |  |
| `items[].totalCriticalAlerts` | number |  |
| `items[].totalCriticalPrevented` | number |  |
| `items[].totalHighAdded` | number |  |
| `items[].totalHighAlerts` | number |  |
| `items[].totalHighPrevented` | number |  |
| `items[].totalLowAdded` | number |  |
| `items[].totalLowAlerts` | number |  |
| `items[].totalLowPrevented` | number |  |
| `items[].totalMediumAdded` | number |  |
| `items[].totalMediumAlerts` | number |  |
| `items[].totalMediumPrevented` | number |  |

## Native endpoint

Through the native Socket API, this operation is `GET /analytics/repo/:name/:filter` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository-analytics.md) for the provider-specific parameters and requirements.

