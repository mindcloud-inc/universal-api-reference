# Productboard: List All Features

Retrieves features from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-features?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "owner": {},
      "parent": {},
      "status": {},
      "timeframe": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the feature is archived. |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Rich-text feature description. |
| `id` | string | Productboard feature identifier. |
| `links` | object | API and HTML links for the feature. |
| `name` | string | Feature name. |
| `owner` | object | Assigned owner information. |
| `parent` | object | Parent hierarchy reference. |
| `status` | object | Feature status object. |
| `timeframe` | object | Planned timeframe metadata. |
| `type` | string | Productboard hierarchy type such as feature or subfeature. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Productboard API, this operation is `GET /features` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-features.md) for the provider-specific parameters and requirements.

