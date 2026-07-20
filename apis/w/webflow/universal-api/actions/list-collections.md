# Webflow: List Collections

Retrieves a list of collections from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-collections?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-collections?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "collections": [
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
| `collections` | array<object> | Collections for the site. |

## Native endpoint

Through the native Webflow API, this operation is `GET /sites/:site_id/collections` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

