# TouchBasePro: Get Campaign Lists And Segments

Retrieves campaign lists and segments from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-campaign-lists-and-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-campaign-lists-and-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-campaign-lists-and-segments?${params}`, {
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
      "lists": [
        [
          {}
        ]
      ],
      "segments": [
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
| `lists[]` | array<object> |  |
| `lists[].listId` | string |  |
| `lists[].name` | string |  |
| `segments[]` | array<object> |  |
| `segments[].listId` | string |  |
| `segments[].segmentId` | string |  |
| `segments[].title` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/campaigns/{campaignId}/listsandsegments` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-lists-and-segments.md) for the provider-specific parameters and requirements.

