# LinkTwin: Get Pixel

Retrieves a pixel and its assigned links from LinkTwin.

```
GET https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-pixel?connectionId=$CONNECTION_ID&limit=25&offset=0&id=493" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "493"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-pixel?${params}`, {
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
| `id` | string | yes | Example: `493`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentpage": 1,
      "maxpage": 1,
      "nextpage": {},
      "perpage": 1,
      "pixel": {
        "date": "string",
        "id": 1,
        "name": "Ava Chen",
        "tag": "string",
        "type": "string"
      },
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentpage` | number |  |
| `maxpage` | number |  |
| `nextpage` | object |  |
| `perpage` | number |  |
| `pixel.date` | string |  |
| `pixel.id` | number |  |
| `pixel.name` | string |  |
| `pixel.tag` | string |  |
| `pixel.type` | string |  |
| `result` | number |  |

## Native endpoint

Through the native LinkTwin API, this operation is `GET /pixel/:id` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-pixel.md) for the provider-specific parameters and requirements.

