# PIMMS: Create Referrals Embed Token

Creates a new referrals embed token in PIMMS.

```
POST https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/create-referrals-embed-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PIMMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/create-referrals-embed-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/create-referrals-embed-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "programId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `programId` | string | yes | Referral program ID used to create the embed token. |
| `partnerId` | string | no |  |
| `tenantId` | string | no |  |
| `partner` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": "2026-05-07T12:00:00.000Z",
      "publicToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | date |  |
| `publicToken` | string |  |

## Native endpoint

Through the native PIMMS API, this operation is `POST /tokens/embed/referrals` (base URL `https://api.pimms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-referrals-embed-token.md) for the provider-specific parameters and requirements.

