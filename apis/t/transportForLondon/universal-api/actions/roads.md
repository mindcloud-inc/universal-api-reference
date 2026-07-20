# Transport for London: List Roads

Retrieves roads managed by Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/roads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/roads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/roads?${params}`, {
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
      "bounds": "string",
      "displayName": "Ava Chen",
      "envelope": "string",
      "id": "string",
      "statusSeverity": "string",
      "statusSeverityDescription": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounds` | string |  |
| `displayName` | string |  |
| `envelope` | string |  |
| `id` | string |  |
| `statusSeverity` | string |  |
| `statusSeverityDescription` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Road` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/roads.md) for the provider-specific parameters and requirements.

