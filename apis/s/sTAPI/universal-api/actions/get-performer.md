# STAPI: Get Performer



```
GET https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-performer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-performer?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-performer?${params}`, {
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
| `uid` | string | yes | Performer unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "performer": {
        "birthName": "Ava Chen",
        "dateOfBirth": "string",
        "gender": "string",
        "name": "Ava Chen",
        "placeOfBirth": "string",
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `performer` | object |  |
| `performer.birthName` | string |  |
| `performer.dateOfBirth` | string |  |
| `performer.gender` | string |  |
| `performer.name` | string |  |
| `performer.placeOfBirth` | string |  |
| `performer.uid` | string |  |

## Native endpoint

Through the native STAPI API, this operation is `GET /v2/rest/performer` (base URL `https://stapi.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-performer.md) for the provider-specific parameters and requirements.

