# Process Street: List Data Sets



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-data-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-data-sets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-data-sets?${params}`, {
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
      "audit": {},
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audit` | object |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `organizationId` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /data-sets` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-sets.md) for the provider-specific parameters and requirements.

