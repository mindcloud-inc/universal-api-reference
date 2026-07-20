# IceCubes: Get Meeting Insights



```
GET https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-meeting-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-meeting-insights?connectionId=$CONNECTION_ID&meetingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-meeting-insights?${params}`, {
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
| `meetingId` | string | yes | The meeting ID to retrieve insights for. |
| `category` | string | no | Filter insights by category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "insights": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `insights` | array<object> | AI-extracted sales insights for the meeting. |

## Native endpoint

Through the native IceCubes API, this operation is `GET /meetings/:id/insights` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-insights.md) for the provider-specific parameters and requirements.

