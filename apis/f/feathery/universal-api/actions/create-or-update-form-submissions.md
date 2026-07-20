# Feathery: Create or Update Form Submissions



```
POST https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-or-update-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-or-update-form-submissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-or-update-form-submissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | object | yes | A mapping from field identifier to value. |
| `user_id` | string | no | A new or existing user ID. If omitted, Feathery generates one. |
| `forms[]` | array<string> | no | An array of form IDs to initialize submissions for. |
| `complete` | boolean | no | Whether the submission should be marked complete. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documents[]` | array<object> | no | An array of document generation objects, optionally with output locations for spreadsheet cells. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "complete": true,
      "documents": [
        {}
      ],
      "fields": {},
      "forms": [
        "string"
      ],
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `complete` | boolean |  |
| `documents` | array<object> |  |
| `fields` | object |  |
| `forms` | array<string> |  |
| `user_id` | string |  |

## Native endpoint

Through the native Feathery API, this operation is `POST /api/form/submission/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-form-submissions.md) for the provider-specific parameters and requirements.

