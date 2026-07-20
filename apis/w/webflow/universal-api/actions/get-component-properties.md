# Webflow: Get Component Properties

Retrieves properties for a component from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-component-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-component-properties?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string&componentId=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-component-properties?${params}`, {
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
| `localeId` | string | no | The locale identifier for localized properties. |
| `branchId` | string | no | The branch identifier for branch content. |
| `limit` | number | no | Maximum number of properties to return. |
| `offset` | number | no | Number of properties to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "componentId": "string",
      "pagination": {},
      "properties": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `componentId` | string | Component ID. |
| `pagination` | object | Pagination metadata for properties. |
| `properties` | array<object> | Component property definitions. |

## Native endpoint

Through the native Webflow API, this operation is `GET /sites/:site_id/components/:component_id/properties` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-component-properties.md) for the provider-specific parameters and requirements.

