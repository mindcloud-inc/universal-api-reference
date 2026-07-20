# Xata: Resend an invitation



```
POST https://connect.mindcloud.co/v1/universal/xata/latest/actions/resend-organization-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xata/latest/actions/resend-organization-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "invitationID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/resend-organization-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "invitationID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes | Unique identifier for a specific organization |
| `invitationID` | string | yes | Unique identifier for an invitation |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Xata API, this operation is `POST /organizations/:organizationID/invitations/:invitationID/resend` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-organization-invitation.md) for the provider-specific parameters and requirements.

