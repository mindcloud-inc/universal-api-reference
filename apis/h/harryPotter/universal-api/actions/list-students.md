# Harry Potter: List Students

Retrieves Harry Potter student characters.

```
GET https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/list-students
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harry Potter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/list-students?${params}`, {
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
      "actor": "string",
      "alive": true,
      "alternate_actors": [
        "string"
      ],
      "alternate_names": [
        "Ava Chen"
      ],
      "ancestry": "string",
      "dateOfBirth": "string",
      "eyeColour": "string",
      "gender": "string",
      "hairColour": "string",
      "hogwartsStaff": true,
      "hogwartsStudent": true,
      "house": "string",
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "patronus": "string",
      "species": "string",
      "wand": {},
      "wizard": true,
      "yearOfBirth": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor` | string |  |
| `alive` | boolean |  |
| `alternate_actors` | array<string> |  |
| `alternate_names` | array<string> |  |
| `ancestry` | string |  |
| `dateOfBirth` | string |  |
| `eyeColour` | string |  |
| `gender` | string |  |
| `hairColour` | string |  |
| `hogwartsStaff` | boolean |  |
| `hogwartsStudent` | boolean |  |
| `house` | string |  |
| `id` | string |  |
| `image` | string |  |
| `name` | string |  |
| `patronus` | string |  |
| `species` | string |  |
| `wand` | object |  |
| `wizard` | boolean |  |
| `yearOfBirth` | number |  |

## Native endpoint

Through the native Harry Potter API, this operation is `GET /api/characters/students` (base URL `https://hp-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students.md) for the provider-specific parameters and requirements.

