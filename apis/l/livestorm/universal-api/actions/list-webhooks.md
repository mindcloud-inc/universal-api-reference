# Livestorm: List Webhooks

Retrieves webhooks from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-webhooks?${params}`, {
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
| `filter[event]` | string | no | Filter Webhooks by event : event.published, event.created, session.started, session.ended, session.created, people.registered, people.attended, people.not_attended, people.watched_replay, job.ended |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": 1,
        "event": "string",
        "updatedAt": 1,
        "url": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | number |  |
| `attributes.event` | string |  |
| `attributes.updatedAt` | number |  |
| `attributes.url` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Livestorm API, this operation is `GET webhooks` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

