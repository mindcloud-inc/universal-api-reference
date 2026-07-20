# Common Ninja: List Widgets

Retrieves user widgets from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/list-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/list-widgets?${params}`, {
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
| `fields` | string | no | Comma-separated list of fields to include in the response. |
| `limit` | number | no | Maximum number of widgets to return. |
| `projectId` | string | no | Filter widgets by project ID. |
| `query` | string | no | Filter widgets by search query. |
| `type` | string | no | Filter widgets by widget type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {}
      ],
      "limit": 1,
      "nextPage": 1,
      "page": 1,
      "pages": 1,
      "prevPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> |  |
| `limit` | number |  |
| `nextPage` | number |  |
| `page` | number |  |
| `pages` | number |  |
| `prevPage` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /widgets` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-widgets.md) for the provider-specific parameters and requirements.

