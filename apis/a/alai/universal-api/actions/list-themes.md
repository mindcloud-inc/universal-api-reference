# Alai: List Themes

Retrieves theme IDs and names from Alai.

```
GET https://connect.mindcloud.co/v1/universal/alai/latest/actions/list-themes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alai/latest/actions/list-themes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alai/latest/actions/list-themes?${params}`, {
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
      "themes": [
        {
          "id": "string",
          "name": "Ava Chen"
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
| `themes[].id` | string |  |
| `themes[].name` | string |  |

## Native endpoint

Through the native Alai API, this operation is `GET /themes` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-themes.md) for the provider-specific parameters and requirements.

