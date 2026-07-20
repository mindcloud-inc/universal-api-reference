# Tiliter: List Archetypes

Retrieves archetypes from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-archetypes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-archetypes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-archetypes?${params}`, {
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
      "archetypes": [
        {
          "alternateNames": [
            "Ava Chen"
          ],
          "department": "string",
          "description": "string",
          "exampleImages": [
            "string"
          ],
          "feature1": "string",
          "feature2": "string",
          "id": "string",
          "keywords": [
            "string"
          ],
          "type": "string",
          "variety": "string"
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
| `archetypes` | array<object> |  |
| `archetypes[].alternateNames` | array |  |
| `archetypes[].department` | string |  |
| `archetypes[].description` | string |  |
| `archetypes[].exampleImages` | array<string> |  |
| `archetypes[].exampleImages[]` | string |  |
| `archetypes[].feature1` | string |  |
| `archetypes[].feature2` | string |  |
| `archetypes[].id` | string |  |
| `archetypes[].keywords` | array |  |
| `archetypes[].type` | string |  |
| `archetypes[].variety` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /archetypes/` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-archetypes.md) for the provider-specific parameters and requirements.

