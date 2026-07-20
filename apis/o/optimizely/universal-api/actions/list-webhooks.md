# Optimizely: List Webhooks

Retrieves webhooks for a project in Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "4844790198566912"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-webhooks?${params}`, {
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
| `projectId` | string | yes | The project id to list webhooks for. Default: `4844790198566912`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": "string",
      "description": "string",
      "id": 1,
      "lastModified": "string",
      "name": "Ava Chen",
      "projectId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | string |  |
| `description` | string |  |
| `id` | number |  |
| `lastModified` | string |  |
| `name` | string |  |
| `projectId` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /projects/{projectId}/webhooks` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

