# Productboard: Get Feature

Retrieves a feature from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-feature?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-feature?${params}`, {
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
| `id` | string | yes | Feature ID from Productboard. |

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
      "lastHealthUpdate": {},
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
| `lastHealthUpdate` | object | Most recent health update when present. |
| `links` | object | API and HTML links for the feature. |
| `name` | string | Feature name. |
| `owner` | object | Assigned owner information. |
| `parent` | object | Parent hierarchy reference. |
| `status` | object | Feature status object. |
| `timeframe` | object | Planned timeframe metadata. |
| `type` | string | Hierarchy type such as feature or subfeature. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Productboard API, this operation is `GET /features/:id` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature.md) for the provider-specific parameters and requirements.

