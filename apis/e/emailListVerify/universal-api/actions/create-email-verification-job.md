# EmailListVerify: Create Email Verification Job

Creates an asynchronous email verification job in EmailListVerify.

```
POST https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-email-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-email-verification-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-email-verification-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to verify asynchronously. |
| `quality` | string | no | Verification quality. Standard costs 1 credit; high costs 2 credits and can take longer. One of: `0`, `1`. Default: `standard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "quality": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email submitted for asynchronous verification. |
| `id` | string | Created email verification job ID. |
| `quality` | string | Verification quality. |

## Native endpoint

Through the native EmailListVerify API, this operation is `POST /api/emailJobs` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-verification-job.md) for the provider-specific parameters and requirements.

