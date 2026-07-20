# Pipeless Recommendations: Edit Object

Updates an existing object in Pipeless Recommendations.

```
PUT https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/edit-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/edit-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "1885"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/edit-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "1885"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Numeric Pipeless app ID. Default: `1885`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `id` | string |  |
| `modifiedOn` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `PATCH /v1/apps/:appId/objects` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-object.md) for the provider-specific parameters and requirements.

