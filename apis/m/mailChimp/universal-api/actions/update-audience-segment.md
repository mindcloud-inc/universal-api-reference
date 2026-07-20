# Mailchimp: Update Audience Segment

Updates an existing segment in a Mailchimp audience.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-audience-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-audience-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "name": "Ava Chen",
  "segment_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-audience-segment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "string",
    "name": "Ava Chen",
    "segment_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `name` | string | yes | Segment name. |
| `options` | object | no | Segment options object. |
| `segment_id` | string | yes | The unique ID for the audience segment. |
| `static_segment[]` | array<string> | no | Static segment member list. |
| `options.match` | list<string> | no | Match type for segment conditions (any or all). One of: `all`, `any`. |
| `options.conditions[]` | array<object> | no | Array of segment condition objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "listId": "string",
      "memberCount": 1,
      "name": "Ava Chen",
      "options": {},
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
| `createdAt` | date |  |
| `id` | number |  |
| `listId` | string |  |
| `memberCount` | number |  |
| `name` | string |  |
| `options` | object |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mailchimp API, this operation is `PATCH lists/:list_id/segments/:segment_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-audience-segment.md) for the provider-specific parameters and requirements.

