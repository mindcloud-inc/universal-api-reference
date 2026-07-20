# Emailable: Create Verification Batch

Creates an email verification batch in Emailable.

```
POST https://connect.mindcloud.co/v1/universal/emailable/latest/actions/create-verification-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/create-verification-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "alice@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailable/latest/actions/create-verification-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "alice@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails` | string | yes | One or more email addresses to verify in the batch. Accepts multiple values in one string, delimited by `,`. Example: `alice@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional URL that receives the completed batch result via HTTP POST. Example: `https://example.com/webhooks/emailable`. |
| `retries` | boolean | no | Leave enabled to retry certain mail-server responses for better accuracy. |
| `responseFields` | string | no | Optional list of per-email response fields to include in the batch result. Accepts multiple values in one string, delimited by `,`. Example: `email,state,score`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The Emailable batch identifier for the newly created verification batch. |
| `message` | string | Confirmation message returned after the batch is created. |

## Native endpoint

Through the native Emailable API, this operation is `POST /v1/batch` (base URL `https://api.emailable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-verification-batch.md) for the provider-specific parameters and requirements.

