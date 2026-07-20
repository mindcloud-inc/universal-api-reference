# Listclean: Verify Batch Of Emails

Verifies up to 3,000 email addresses in Listclean.

```
POST https://connect.mindcloud.co/v1/universal/listclean/latest/actions/verify-batch-of-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/verify-batch-of-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": "person@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listclean/latest/actions/verify-batch-of-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": "person@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Email addresses to verify. The Listclean API accepts up to 3000 emails. Example: `person@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list_id` | number | Verification list ID created for the batch request. |

## Native endpoint

Through the native Listclean API, this operation is `POST /verify/email/batch` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-batch-of-emails.md) for the provider-specific parameters and requirements.

