# smsmode: Update Channel



```
PUT https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationId": "string",
  "channelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationId": "string",
    "channelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationId` | string | yes | Organisation ID path parameter from the smsmode API route. |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `name` | string | no | Name request body field documented by the smsmode API. |
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
      "name": "Ava Chen"
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
| `name` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `PATCH commons/v1/organisations/:organisationId/channels/:channelId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

