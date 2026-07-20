# Otiom: List Helpers

Retrieves helpers from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-helpers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-helpers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-helpers?${params}`, {
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
      "alias": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "helper_for_otiom_user_ids": [
        "string"
      ],
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `avatar` | string |  |
| `email` | string |  |
| `helper_for_otiom_user_ids` | array |  |
| `id` | number |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/helpers/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-helpers.md) for the provider-specific parameters and requirements.

