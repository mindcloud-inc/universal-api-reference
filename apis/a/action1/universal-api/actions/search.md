# Action1: Search

Finds Action1 objects in an organization by query.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/search?connectionId=$CONNECTION_ID&orgId=string&query=server%20patch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "query": "server patch"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/search?${params}`, {
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
| `orgId` | string | yes | Provide an organization ID. Most API calls are scoped to one organization. |
| `query` | string | yes | Provide a query for searching. Example: `server patch`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertable": "string",
      "builtin": "string",
      "children": "string",
      "dataSources": [
        {}
      ],
      "description": "string",
      "id": "string",
      "largeImage": "string",
      "longDescription": "string",
      "name": "Ava Chen",
      "parentCategory": "string",
      "reportData": "string",
      "reportErrors": "string",
      "self": "string",
      "simple": "string",
      "smallImage": "string",
      "summaryCustomizable": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertable` | string |  |
| `builtin` | string |  |
| `children` | string |  |
| `dataSources` | array<object> |  |
| `description` | string |  |
| `id` | string |  |
| `largeImage` | string |  |
| `longDescription` | string |  |
| `name` | string |  |
| `parentCategory` | string |  |
| `reportData` | string |  |
| `reportErrors` | string |  |
| `self` | string |  |
| `simple` | string |  |
| `smallImage` | string |  |
| `summaryCustomizable` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /search/:orgId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

