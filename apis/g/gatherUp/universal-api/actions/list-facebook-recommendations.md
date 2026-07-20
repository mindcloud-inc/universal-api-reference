# GatherUp: List Facebook Recommendations

Retrieves Facebook recommendations received in GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-facebook-recommendations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-facebook-recommendations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-facebook-recommendations?${params}`, {
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
| `businessId` | number | no | Business id (or multiple comma-separated ids.) |
| `from` | string | no | Received from |
| `to` | string | no | Received to |
| `page` | number | no | Page Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "businessId": "string",
      "content": "string",
      "count": "string",
      "errorCode": 1,
      "errorMessage": "string",
      "id": "string",
      "page": 1,
      "pages": 1,
      "perPage": 1,
      "recommendation": "string",
      "recommendations": [
        {}
      ],
      "time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `businessId` | string |  |
| `content` | string |  |
| `count` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `id` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `perPage` | number |  |
| `recommendation` | string |  |
| `recommendations` | array<object> |  |
| `time` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /facebook-recommendations/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-facebook-recommendations.md) for the provider-specific parameters and requirements.

