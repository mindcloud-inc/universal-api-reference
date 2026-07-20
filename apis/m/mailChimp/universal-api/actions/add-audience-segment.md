# Mailchimp: Add Audience Segment

Creates a new segment in a Mailchimp audience.

```
POST https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "string",
    "name": "Ava Chen"
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

Through the native Mailchimp API, this operation is `POST lists/:list_id/segments` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-audience-segment.md) for the provider-specific parameters and requirements.

