# MoreApp: Resend Invite

Resends an invite in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/resend-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/resend-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/resend-invite', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Empty response body on successful invite resend; presence indicates the request completed. |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v2/customers/{{customerId}}/invites/{{id}}/resend` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-invite.md) for the provider-specific parameters and requirements.

