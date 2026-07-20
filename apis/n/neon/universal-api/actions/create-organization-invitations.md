# Neon: Create organization invitations

Creates organization invitations in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-organization-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-organization-invitations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "org_id": "string",
  "invitations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-organization-invitations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "org_id": "string",
    "invitations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `org_id` | string | yes | Neon API parameter org_id |
| `invitations[]` | array<object> | yes | Neon API parameter invitations |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invitations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invitations` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `POST /organizations/:org_id/invitations` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-invitations.md) for the provider-specific parameters and requirements.

