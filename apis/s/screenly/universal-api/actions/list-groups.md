# Screenly: List Groups

Retrieves groups from Screenly.

```
GET https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-groups?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "screens": [
        {
          "coords": [
            1
          ],
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `screens[].coords[]` | number |  |
| `screens[].id` | string |  |
| `screens[].name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Screenly API, this operation is `GET /groups/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

