# Webflow: Update Component Content

Updates content for a component in Webflow.

```
PUT https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-component-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-component-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "componentId": "string",
  "nodes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-component-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "componentId": "string",
    "nodes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | The unique identifier of the site. |
| `componentId` | string | yes | The unique identifier of the component. |
| `nodes` | list<object> | yes | List of component DOM nodes to update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `localeId` | string | no | The locale identifier for localized content. |
| `branchId` | string | no | The branch identifier for branch content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Validation errors returned by the update component content request. |

## Native endpoint

Through the native Webflow API, this operation is `POST /sites/:site_id/components/:component_id/dom` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-component-content.md) for the provider-specific parameters and requirements.

