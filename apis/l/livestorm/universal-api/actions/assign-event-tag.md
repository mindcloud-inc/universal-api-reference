# Livestorm: Assign Event Tag

Assigns a tag to an event in Livestorm.

```
POST https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/assign-event-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/assign-event-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data.attributes.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/assign-event-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data.attributes.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Event ID |
| `data.attributes.title` | string | yes | Tag title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "title": "string"
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
| `attributes.title` | string | Tag title |
| `id` | string | Tag ID |
| `type` | string |  |

## Native endpoint

Through the native Livestorm API, this operation is `POST events/:id/tags` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-event-tag.md) for the provider-specific parameters and requirements.

