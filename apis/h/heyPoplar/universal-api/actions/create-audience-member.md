# HeyPoplar: Create Audience Member

Creates an audience member in HeyPoplar.

```
POST https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-audience-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audienceId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-audience-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audienceId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audienceId` | string | yes | ID of the audience to add the member to. |
| `email` | string | yes | Email address for the audience member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "email_sha256": "ava@example.com",
      "external_id": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `email_sha256` | string |  |
| `external_id` | string |  |
| `id` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `POST /audience/:id` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audience-member.md) for the provider-specific parameters and requirements.

