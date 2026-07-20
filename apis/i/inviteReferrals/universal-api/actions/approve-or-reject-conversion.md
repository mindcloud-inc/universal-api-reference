# InviteReferrals: Approve Or Reject Conversion



```
PUT https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/approve-or-reject-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InviteReferrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/approve-or-reject-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "campaignId": 1,
  "event": "string",
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/approve-or-reject-conversion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "campaignId": 1,
    "event": "string",
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Order identifier of the conversion to confirm or reject. |
| `campaignId` | number | yes | InviteReferrals campaign identifier. |
| `event` | string | yes | Conversion event name associated with the order. |
| `status` | number | yes | Set to approve or reject the conversion based on InviteReferrals docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native InviteReferrals API, this operation is `POST /conversion/confirm` (base URL `https://www.ref-r.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-or-reject-conversion.md) for the provider-specific parameters and requirements.

