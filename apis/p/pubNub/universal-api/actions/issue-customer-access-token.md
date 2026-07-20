# PubNub: Issue Customer Access Token

Issues a customer access token in PubNub.

```
POST https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/issue-customer-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/issue-customer-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1,
  "customerUserId": "string",
  "externalId": "string",
  "permissions[0]": "business-object:read"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/issue-customer-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1,
    "customerUserId": "string",
    "externalId": "string",
    "permissions[0]": "business-object:read"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | number | yes | PubNub application ID. |
| `customerUserId` | string | yes | Customer user identifier. |
| `expiresIn` | string | no | Optional token duration such as 1h. Default: `1h`. |
| `externalId` | string | yes | Customer external identifier. |
| `permissions[0]` | string | yes | First permission string. Default: `business-object:read`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PubNub API returns.

## Native endpoint

Through the native PubNub API, this operation is `POST /oem/access-token` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-customer-access-token.md) for the provider-specific parameters and requirements.

