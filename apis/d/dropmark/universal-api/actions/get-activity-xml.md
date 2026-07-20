# Dropmark: Get Activity XML



```
GET https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity-xml?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity-xml?${params}`, {
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
      "content": "string",
      "format": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Raw XML document returned by the activity feed. |
| `format` | string | Feed format identifier. |

## Native endpoint

Through the native Dropmark API, this operation is `GET /activity.xml` (base URL `https://{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-xml.md) for the provider-specific parameters and requirements.

