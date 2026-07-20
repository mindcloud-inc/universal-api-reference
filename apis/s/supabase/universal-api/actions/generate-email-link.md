# Supabase: Generate Email Link

Generates a Supabase Auth email action link.

```
POST https://connect.mindcloud.co/v1/universal/supabase/latest/actions/generate-email-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/generate-email-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/generate-email-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "actionLink": "https://example.com",
      "emailOtp": "ava@example.com",
      "hashedToken": "string",
      "redirectTo": "string",
      "verificationType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionLink` | string |  |
| `emailOtp` | string |  |
| `hashedToken` | string |  |
| `redirectTo` | string |  |
| `verificationType` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `POST /auth/v1/admin/generate_link` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-email-link.md) for the provider-specific parameters and requirements.

