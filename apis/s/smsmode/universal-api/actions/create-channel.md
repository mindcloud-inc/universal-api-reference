# smsmode: Create Channel



```
POST https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationId": "string",
  "name": "Ava Chen",
  "type": "string",
  "flow": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationId": "string",
    "name": "Ava Chen",
    "type": "string",
    "flow": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationId` | string | yes | Organisation ID path parameter from the smsmode API route. |
| `name` | string | yes | Name request body field documented by the smsmode API. |
| `type` | string | yes | Type request body field documented by the smsmode API. |
| `flow` | string | yes | Flow request body field documented by the smsmode API. |
| `dailyConsumptionLimit` | number | no | Daily Consumption Limit request body field documented by the smsmode API. |
| `defaultCallbackUrlStatus` | string | no | Default Status Callback URL request body field documented by the smsmode API. |
| `defaultCallbackUrlMo` | string | no | Default MO Callback URL request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dailyConsumptionLimit": 1,
      "defaultCallbackUrlMo": "https://example.com",
      "defaultCallbackUrlStatus": "https://example.com",
      "flow": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dailyConsumptionLimit` | number |  |
| `defaultCallbackUrlMo` | string |  |
| `defaultCallbackUrlStatus` | string |  |
| `flow` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `POST commons/v1/organisations/:organisationId/channels` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

