# Leadspicker: Get Sequence Message

Retrieves a sequence message from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-sequence-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-sequence-message?connectionId=$CONNECTION_ID&sequenceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sequenceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-sequence-message?${params}`, {
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
| `sequenceId` | number | yes | Leadspicker sequence message identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "after_connection": true,
      "child_relations": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "custom_action_url": "https://example.com",
      "delay_days": 1,
      "delay_hours": 1,
      "id": 1,
      "include_unsubscribe_footer": true,
      "is_quick_followup": true,
      "is_reply": true,
      "message": "string",
      "missing_variables": [
        "string"
      ],
      "outreach_step_type": "string",
      "parent_relations": [
        {}
      ],
      "position": {},
      "preconditions": [
        {}
      ],
      "project_id": 1,
      "rephrase_status": "string",
      "required_sentiment_level": "string",
      "skippable": true,
      "subject": "string",
      "undefined_variables": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `after_connection` | boolean |  |
| `child_relations` | array<object> |  |
| `created` | date |  |
| `custom_action_url` | string |  |
| `delay_days` | number |  |
| `delay_hours` | number |  |
| `id` | number |  |
| `include_unsubscribe_footer` | boolean |  |
| `is_quick_followup` | boolean |  |
| `is_reply` | boolean |  |
| `message` | string |  |
| `missing_variables` | array<string> |  |
| `outreach_step_type` | string |  |
| `parent_relations` | array<object> |  |
| `position` | object |  |
| `preconditions` | array<object> |  |
| `project_id` | number |  |
| `rephrase_status` | string |  |
| `required_sentiment_level` | string |  |
| `skippable` | boolean |  |
| `subject` | string |  |
| `undefined_variables` | array<string> |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/sequence/:sequence_id` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sequence-message.md) for the provider-specific parameters and requirements.

