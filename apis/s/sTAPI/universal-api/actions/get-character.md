# STAPI: Get Character



```
GET https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-character
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-character?${params}`, {
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
| `uid` | string | yes | Character unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "character": {
        "deceased": true,
        "gender": "string",
        "hologram": true,
        "name": "Ava Chen",
        "uid": "string",
        "yearOfBirth": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `character` | object |  |
| `character.deceased` | boolean |  |
| `character.gender` | string |  |
| `character.hologram` | boolean |  |
| `character.name` | string |  |
| `character.uid` | string |  |
| `character.yearOfBirth` | number |  |

## Native endpoint

Through the native STAPI API, this operation is `GET /v1/rest/character` (base URL `https://stapi.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character.md) for the provider-specific parameters and requirements.

