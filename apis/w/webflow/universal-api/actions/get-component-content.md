# Webflow: Get Component Content

Retrieves content for a component from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-component-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-component-content?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string&componentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string",
  "componentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-component-content?${params}`, {
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
| `siteId` | string | yes | The unique identifier of the site. |
| `componentId` | string | yes | The unique identifier of the component. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `localeId` | string | no | The locale identifier for localized content. |
| `branchId` | string | no | The branch identifier for branch content. |
| `limit` | number | no | Maximum number of content nodes to return. |
| `offset` | number | no | Number of content nodes to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "componentId": "string",
      "nodes": [
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
| `componentId` | string | Component ID. |
| `nodes` | array<object> | Component content nodes. |
| `pagination` | object | Pagination metadata for nodes. |

## Native endpoint

Through the native Webflow API, this operation is `GET /sites/:site_id/components/:component_id/dom` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-component-content.md) for the provider-specific parameters and requirements.

