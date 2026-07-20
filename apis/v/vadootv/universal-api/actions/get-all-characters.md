# Vadootv: Get all characters

Retrieves AI characters from Vadootv.

```
GET https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-all-characters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-all-characters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-all-characters?${params}`, {
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
      "": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
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
| `[]` | array<object> | Available AI character records. |
| `[].createdAt` | date | When the character was created. |
| `[].id` | number | Character ID. |
| `[].name` | string | Character display name. |
| `[].url` | string | Character image URL. |

## Native endpoint

Through the native Vadootv API, this operation is `GET /api/get_all_characters` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-characters.md) for the provider-specific parameters and requirements.

