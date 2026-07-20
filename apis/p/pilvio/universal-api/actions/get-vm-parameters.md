# Pilvio: Get VM Parameters



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-vm-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-vm-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-vm-parameters?${params}`, {
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
      "constraint": "string",
      "description": "string",
      "mandatory": true,
      "max": 1,
      "min": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `constraint` | string |  |
| `description` | string |  |
| `mandatory` | boolean |  |
| `max` | number |  |
| `min` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /api/parameters/vm` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vm-parameters.md) for the provider-specific parameters and requirements.

