# HeadshotPro: List Model Photos

Retrieves photos for a model in HeadshotPro.

```
GET https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/list-model-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/list-model-photos?connectionId=$CONNECTION_ID&limit=25&offset=0&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/list-model-photos?${params}`, {
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
| `modelId` | string | yes | ID of the model whose photos should be listed. |
| `status` | string | no | Optional photo status filter. |
| `likedStatus` | string | no | Optional rating filter: none, liked, or loved. |
| `include` | string | no | URL variants to include: main or all. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "photos": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination details for the result page. |
| `photos` | array<object> | Photos returned by the query. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native HeadshotPro API, this operation is `GET /organization/models/:modelId/photos` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-model-photos.md) for the provider-specific parameters and requirements.

