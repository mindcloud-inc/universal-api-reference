# Optimizely: List Changes

Retrieves project change history from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-changes?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "4844790198566912"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-changes?${params}`, {
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
| `projectId` | string | yes | The project id to list change history for. Default: `4844790198566912`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changes": [
        {}
      ],
      "changeType": "string",
      "created": "string",
      "entity": "string",
      "id": 1,
      "projectId": 1,
      "source": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changes` | array<object> |  |
| `changeType` | string |  |
| `created` | string |  |
| `entity` | string |  |
| `id` | number |  |
| `projectId` | number |  |
| `source` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /changes` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-changes.md) for the provider-specific parameters and requirements.

