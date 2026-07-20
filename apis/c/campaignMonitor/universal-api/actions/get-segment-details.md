# Campaign Monitor: Get Segment Details

Retrieves details for a Campaign Monitor segment.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-segment-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-segment-details?connectionId=$CONNECTION_ID&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-segment-details?${params}`, {
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
| `segmentId` | string | yes | Campaign Monitor segment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSubscribers": 1,
      "listId": "string",
      "ruleGroups": [
        {}
      ],
      "segmentId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSubscribers` | number | Number of active subscribers currently matching the segment. |
| `listId` | string | List identifier associated with the segment. |
| `ruleGroups` | array<object> | Segment rule groups defined in Campaign Monitor. |
| `segmentId` | string | Campaign Monitor segment identifier. |
| `title` | string | Segment title. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /segments/:segmentId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment-details.md) for the provider-specific parameters and requirements.

