# Time Doctor: List Categories

Retrieves productivity categories from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-categories?${params}`, {
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
      "entity": "string",
      "id": "string",
      "name": "Ava Chen",
      "scope": "string",
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scope` | string |  |
| `score` | number |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/categories` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

