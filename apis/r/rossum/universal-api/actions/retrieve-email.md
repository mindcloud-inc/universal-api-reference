# Rossum: Retrieve Email

Retrieves an email from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-email?connectionId=$CONNECTION_ID&emailID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-email?${params}`, {
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
| `emailID` | number | yes | ID of the email to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        "string"
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "documents": [
        "string"
      ],
      "id": 1,
      "inbox": "string",
      "queue": "string",
      "subject": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | array<string> | Related annotation URLs. |
| `created_at` | date | Creation timestamp. |
| `documents` | array<string> | Related document URLs. |
| `id` | number | Rossum email ID. |
| `inbox` | string | Inbox URL. |
| `queue` | string | Queue URL. |
| `subject` | string | Email subject. |
| `type` | string | Email type. |
| `url` | string | Email resource URL. |

## Native endpoint

Through the native Rossum API, this operation is `GET /emails/:emailID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-email.md) for the provider-specific parameters and requirements.

