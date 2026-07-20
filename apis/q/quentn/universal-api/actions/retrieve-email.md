# Quentn: Retrieve Email



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-email?connectionId=$CONNECTION_ID&email_id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email_id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-email?${params}`, {
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
| `email_id` | number | yes | The numeric Quentn email id to retrieve. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyHtml": "string",
      "bodyText": "string",
      "context": "string",
      "id": "string",
      "senderId": 1,
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyHtml` | string |  |
| `bodyText` | string |  |
| `context` | string |  |
| `id` | string |  |
| `senderId` | number |  |
| `subject` | string |  |

## Native endpoint

Through the native Quentn API, this operation is `GET /mail/:email_id` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-email.md) for the provider-specific parameters and requirements.

