# OneHash: List Labels

Retrieves account labels from OneHash.

```
GET https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneHash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/list-labels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | no | OneHash Chat account id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payload": [
        {
          "color": "string",
          "description": "string",
          "id": 1,
          "showOnSidebar": true,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payload[].color` | string |  |
| `payload[].description` | string |  |
| `payload[].id` | number |  |
| `payload[].showOnSidebar` | boolean |  |
| `payload[].title` | string |  |

## Native endpoint

Through the native OneHash API, this operation is `GET /api/v1/accounts/:accountId/labels` (base URL `https://chat.onehash.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

