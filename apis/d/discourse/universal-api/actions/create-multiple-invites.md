# Discourse: Create Multiple Invites

Creates multiple user invites in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-multiple-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-multiple-invites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-multiple-invites', {
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
| `email` | string | yes | Comma-separated invitee emails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed_invitations": [
        {}
      ],
      "num_failed_invitations": 1,
      "num_successfully_created_invitations": 1,
      "successful_invitations": [
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
| `failed_invitations` | array<object> |  |
| `num_failed_invitations` | number |  |
| `num_successfully_created_invitations` | number |  |
| `successful_invitations` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /invites/create-multiple.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-invites.md) for the provider-specific parameters and requirements.

