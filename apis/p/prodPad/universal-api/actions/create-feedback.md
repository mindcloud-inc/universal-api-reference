# ProdPad: Create Feedback

Creates new feedback in ProdPad.

```
POST https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedback": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedback": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedback` | string | yes |  |
| `contactId` | string | no |  |
| `name` | string | no |  |
| `companyId` | string | no |  |
| `email` | string | no |  |
| `about` | string | no |  |
| `source` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "feedbacks": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "feedback": "string",
          "id": 1,
          "source": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        }
      ],
      "id": 1,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `feedbacks[].created_at` | date |  |
| `feedbacks[].feedback` | string |  |
| `feedbacks[].id` | number |  |
| `feedbacks[].source` | string |  |
| `feedbacks[].updated_at` | date |  |
| `feedbacks[].uuid` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProdPad API, this operation is `POST /feedbacks` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

