# Ziflow: List Proof Emails

Retrieves proof emails from Ziflow by proof ID.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-emails?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-emails?${params}`, {
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
| `id` | string | yes | The proof ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "emails": [
        {
          "content_url": "ava@example.com",
          "from": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          },
          "sent_at": "2026-05-07T12:00:00.000Z",
          "subject": "ava@example.com",
          "to": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "has_more": true,
      "page": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `emails[].content_url` | string |  |
| `emails[].from.address` | string |  |
| `emails[].from.name` | string |  |
| `emails[].sent_at` | date |  |
| `emails[].subject` | string |  |
| `emails[].to.address` | string |  |
| `emails[].to.name` | string |  |
| `has_more` | boolean |  |
| `page` | number |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /proofs/:id/emails` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-proof-emails.md) for the provider-specific parameters and requirements.

