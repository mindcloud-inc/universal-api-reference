# Bannerbite: Get Scene Data

Retrieves scene data for a Bannerbite bite.

```
GET https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/get-scene-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/get-scene-data?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/get-scene-data?${params}`, {
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
| `id` | number | yes | The Bannerbite bite ID whose scene data you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "color": "string",
          "name": "Ava Chen",
          "value": "string"
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
| `data[].color` | string |  |
| `data[].name` | string |  |
| `data[].value` | string |  |

## Native endpoint

Through the native Bannerbite API, this operation is `GET /api/sceneData/:id` (base URL `https://api.bannerbite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scene-data.md) for the provider-specific parameters and requirements.

