# Sertifier: Delete Recipient

Deletes an existing recipient from Sertifier.

```
DELETE https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/delete-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/delete-recipient?connectionId=$CONNECTION_ID&recipient_id=Recipient%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipient_id": "Recipient ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/delete-recipient?${params}`, {
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
| `recipient_id` | string | yes | Example: `Recipient ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": true,
      "hasError": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | boolean |  |
| `hasError` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `DELETE /recipient/:recipient_id` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-recipient.md) for the provider-specific parameters and requirements.

