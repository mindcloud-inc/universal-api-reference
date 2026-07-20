# Salesrobot: Get LinkedIn Auth URL



```
POST https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/get-linked-in-auth-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesrobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/get-linked-in-auth-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailId": "ava@example.com",
  "timeZone": "America/New_York"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/get-linked-in-auth-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailId": "ava@example.com",
    "timeZone": "America/New_York"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailId` | string | yes | LinkedIn email address to onboard |
| `billAccount` | boolean | no | Whether to bill the connected LinkedIn account Default: `true`. |
| `editAccount` | boolean | no | Whether this is an existing account edit flow Default: `false`. |
| `timeZone` | string | yes | IANA time zone for the account Default: `America/New_York`. |
| `domain` | string | no | Origin domain for the onboarding flow Default: `app.salesrobot.co`. |
| `path` | string | no | Origin path for the onboarding flow Default: `/`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesrobot API returns.

## Native endpoint

Through the native Salesrobot API, this operation is `POST /api/linkedin/account/auth` (base URL `https://api.boomtechinc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-in-auth-url.md) for the provider-specific parameters and requirements.

