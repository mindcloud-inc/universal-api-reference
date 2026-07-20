# Reamaze: List Incidents



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-incidents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-incidents?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "incidentsSystems": [
        {}
      ],
      "status": "string",
      "title": "string",
      "updatedAt": "string",
      "updates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `incidentsSystems` | array<object> |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /incidents` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

