# Automatic Data Extraction: Get Zyte API Stats

Retrieves Zyte API usage stats from Automatic Data Extraction.

```
GET https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/get-zyte-api-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automatic Data Extraction `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/get-zyte-api-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/get-zyte-api-stats?${params}`, {
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
      "date": {},
      "organization_id": {},
      "requests": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | object |  |
| `organization_id` | object |  |
| `requests` | object |  |

## Native endpoint

Through the native Automatic Data Extraction API, this operation is `GET https://zyte-api-stats.zyte.com/api/stats` (base URL `https://api.zyte.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zyte-api-stats.md) for the provider-specific parameters and requirements.

