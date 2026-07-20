# Harry Potter: Get Character By ID

Retrieves a Harry Potter character by ID.

```
GET https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/get-character-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harry Potter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/get-character-by-id?connectionId=$CONNECTION_ID&id=e.g.%209e3f7ce4-b9a7-4244-b709-dae5c1f1d4a8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. 9e3f7ce4-b9a7-4244-b709-dae5c1f1d4a8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/get-character-by-id?${params}`, {
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
| `id` | string | yes | Unique character ID returned by character list actions. Example: `e.g. 9e3f7ce4-b9a7-4244-b709-dae5c1f1d4a8`. |

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

Through the native Harry Potter API, this operation is `GET /api/character/:id` (base URL `https://hp-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character-by-id.md) for the provider-specific parameters and requirements.

