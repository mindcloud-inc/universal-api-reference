# Webflow: List Components

Retrieves a list of components from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-components?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-components?${params}`, {
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
| `siteId` | string | yes | Unique identifier for a Site. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchId` | string | no | Unique identifier for a branch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | array<object> | Components returned for the site. |
| `pagination` | object | Pagination metadata for the component list. |

## Native endpoint

Through the native Webflow API, this operation is `GET /sites/:site_id/components` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-components.md) for the provider-specific parameters and requirements.

