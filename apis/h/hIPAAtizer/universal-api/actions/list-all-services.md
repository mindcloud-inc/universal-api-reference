# HIPAAtizer: List All Services

Retrieves all available services from HIPAAtizer.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-services?${params}`, {
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
      "blockMinutesAfterNow": 1,
      "borderOfDays": 1,
      "duration": 1,
      "id": "string",
      "limit": 1,
      "price": 1,
      "timeBlockAfter": 1,
      "timeBlockBefore": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockMinutesAfterNow` | number |  |
| `borderOfDays` | number |  |
| `duration` | number |  |
| `id` | string |  |
| `limit` | number |  |
| `price` | number |  |
| `timeBlockAfter` | number |  |
| `timeBlockBefore` | number |  |
| `title` | string |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `GET /api/v1/api_key/services/all` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-services.md) for the provider-specific parameters and requirements.

