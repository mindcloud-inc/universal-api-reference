# Harry Potter API: List Students



```
GET https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-students
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harry Potter API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-students?${params}`, {
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
          "alive": true,
          "gender": "string",
          "house": "string",
          "id": "string",
          "image": "string",
          "name": "Ava Chen",
          "species": "string"
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
| `[]` | array<object> | Character records. |
| `[].alive` | boolean | alive |
| `[].gender` | string | gender |
| `[].house` | string | house |
| `[].id` | string | id |
| `[].image` | string | image |
| `[].name` | string | name |
| `[].species` | string | species |

## Native endpoint

Through the native Harry Potter API API, this operation is `GET /api/characters/students` (base URL `https://hp-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students.md) for the provider-specific parameters and requirements.

