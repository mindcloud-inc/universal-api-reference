# Final Space: List Locations



```
GET https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Final Space `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-locations?${params}`, {
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
          "id": 1,
          "img_url": "https://example.com",
          "inhabitants": [
            "string"
          ],
          "name": "Ava Chen",
          "notable_residents": [
            "string"
          ],
          "type": "string"
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
| `[]` | array<object> |  |
| `[].id` | number |  |
| `[].img_url` | string |  |
| `[].inhabitants` | array<string> |  |
| `[].name` | string |  |
| `[].notable_residents` | array<string> |  |
| `[].type` | string |  |

## Native endpoint

Through the native Final Space API, this operation is `GET /location` (base URL `https://finalspaceapi.com/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

