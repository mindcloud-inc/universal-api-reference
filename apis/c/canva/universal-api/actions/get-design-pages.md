# Canva: Get Design Pages

Retrieves pages for a Canva design.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&designId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "designId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-pages?${params}`, {
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
| `designId` | string | yes | The Canva design ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimensions": {
        "height": 1,
        "width": 1
      },
      "index": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensions.height` | number |  |
| `dimensions.width` | number |  |
| `index` | number |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/designs/:designId/pages` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-design-pages.md) for the provider-specific parameters and requirements.

