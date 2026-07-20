# Instant: Create Custom Magic Code

Creates a custom magic code in Instant.

```
POST https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-custom-magic-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-custom-magic-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-custom-magic-code', {
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
| `email` | string | yes | User email address to create a magic code for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Magic code issued by Instant. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/magic_code` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-magic-code.md) for the provider-specific parameters and requirements.

