# Mailchimp: Get Audience Segment

Retrieves a segment from a Mailchimp audience.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience-segment?connectionId=$CONNECTION_ID&list_id=string&segment_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "string",
  "segment_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience-segment?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `include_cleaned` | boolean | no |  |
| `include_transactional` | boolean | no |  |
| `include_unsubscribed` | boolean | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `segment_id` | string | yes | The unique ID for the audience segment. |

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

Through the native Mailchimp API, this operation is `GET lists/:list_id/segments/:segment_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audience-segment.md) for the provider-specific parameters and requirements.

