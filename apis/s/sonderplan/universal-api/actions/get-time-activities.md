# Sonderplan: Get Time Activities



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-time-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-time-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-time-activities?${params}`, {
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
      "created": 1,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /time-activity` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-activities.md) for the provider-specific parameters and requirements.

