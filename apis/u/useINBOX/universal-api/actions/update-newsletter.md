# UseINBOX: Update Newsletter

Updates an existing newsletter in UseINBOX.

```
PUT https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-newsletter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-newsletter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Newsletter ID from INBOX. |
| `subject` | string | no | Updated newsletter subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "htmlContent": "string",
      "id": "string",
      "language": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `htmlContent` | string |  |
| `id` | string |  |
| `language` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native UseINBOX API, this operation is `PATCH /inbox/v1/newsletters/:id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-newsletter.md) for the provider-specific parameters and requirements.

