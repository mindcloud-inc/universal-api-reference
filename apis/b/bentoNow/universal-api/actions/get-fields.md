# Bento Now: Get Fields

Retrieves custom fields from Bento Now.

```
GET https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-fields?${params}`, {
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
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "key": "string",
        "name": "Ava Chen",
        "whitelisted": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | date |  |
| `attributes.key` | string |  |
| `attributes.name` | string |  |
| `attributes.whitelisted` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bento Now API, this operation is `GET /v1/fetch/fields` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fields.md) for the provider-specific parameters and requirements.

