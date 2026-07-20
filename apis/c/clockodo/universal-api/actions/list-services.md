# Clockodo: List Services

Retrieves services from your Clockodo account.

```
GET https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockodo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-services?${params}`, {
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
      "active": true,
      "billableDefault": true,
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billableDefault` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `number` | string |  |

## Native endpoint

Through the native Clockodo API, this operation is `GET /services` (base URL `https://my.clockodo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

