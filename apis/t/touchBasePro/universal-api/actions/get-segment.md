# TouchBasePro: Get Segment

Retrieves a segment from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-segment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-segment?${params}`, {
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
      "activeSubscribers": 1,
      "listId": "string",
      "ruleGroups": [
        [
          {}
        ]
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
| `activeSubscribers` | number |  |
| `listId` | string |  |
| `ruleGroups[]` | array<object> |  |
| `ruleGroups[].rules[]` | array<object> |  |
| `ruleGroups[].rules[].clause` | string |  |
| `ruleGroups[].rules[].ruleType` | string |  |
| `segmentId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/segments/{segmentId}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment.md) for the provider-specific parameters and requirements.

