# BotHelp: Add Subscriber To Funnel By CUID

Adds a subscriber to a funnel by CUID in BotHelp.

```
PUT https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/add-subscriber-to-funnel-by-cuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/add-subscriber-to-funnel-by-cuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "funnelReferral": "string",
  "subscriber_cuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/add-subscriber-to-funnel-by-cuid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "funnelReferral": "string",
    "subscriber_cuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `funnelReferral` | string | yes | Sequence/funnel referral to add the subscriber to. |
| `subscriber_cuid` | string | yes | BotHelp subscriber CUID. |

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
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native BotHelp API, this operation is `POST /v1/subscribers/cuid/:subscriber_cuid/funnel` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber-to-funnel-by-cuid.md) for the provider-specific parameters and requirements.

