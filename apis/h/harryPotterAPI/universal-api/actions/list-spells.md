# Harry Potter API: List Spells



```
GET https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-spells
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harry Potter API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-spells?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-spells?${params}`, {
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
          "description": "string",
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
| `[]` | array<object> | Spell records. |
| `[].description` | string | Spell description. |
| `[].id` | string | Spell identifier. |
| `[].name` | string | Spell name. |

## Native endpoint

Through the native Harry Potter API API, this operation is `GET /api/spells` (base URL `https://hp-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spells.md) for the provider-specific parameters and requirements.

