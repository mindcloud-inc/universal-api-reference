# Harry Potter API: List Characters by House



```
GET https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-characters-by-house
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harry Potter API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-characters-by-house?connectionId=$CONNECTION_ID&house=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "house": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/list-characters-by-house?${params}`, {
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
| `house` | string | yes | Hogwarts house. |

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

Through the native Harry Potter API API, this operation is `GET /api/characters/house/:house` (base URL `https://hp-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-characters-by-house.md) for the provider-specific parameters and requirements.

