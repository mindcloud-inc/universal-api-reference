# BASIC: Get specific API key

Retrieves a specific API key from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-specific-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-specific-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-specific-api-key?${params}`, {
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
      "key": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "label": "string",
        "roles": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key.created_at` | date |  |
| `key.id` | string |  |
| `key.label` | string |  |
| `key.roles` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/{id}/key/{key_id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-specific-api-key.md) for the provider-specific parameters and requirements.

