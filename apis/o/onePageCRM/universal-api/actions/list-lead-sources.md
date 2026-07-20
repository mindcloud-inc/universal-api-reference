# OnePageCRM: List Lead Sources

Retrieves lead sources from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-lead-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-lead-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-lead-sources?${params}`, {
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
      "actionStreamCount": 1,
      "counts": 1,
      "id": "string",
      "teamCounts": [
        {
          "counts": 1,
          "userId": "string"
        }
      ],
      "text": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionStreamCount` | number |  |
| `counts` | number |  |
| `id` | string |  |
| `teamCounts[].counts` | number |  |
| `teamCounts[].userId` | string |  |
| `text` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /lead_sources` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-sources.md) for the provider-specific parameters and requirements.

