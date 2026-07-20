# smsmode: Update Scheduled RCS Campaign



```
PUT https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-scheduled-rcs-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-scheduled-rcs-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-scheduled-rcs-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | string | yes | Campaign ID path parameter from the smsmode API route. |
| `name` | string | no | Name request body field documented by the smsmode API. |
| `sentDate` | date | no | Send Date request body field documented by the smsmode API. |
| `endDate` | date | no | End Date request body field documented by the smsmode API. |
| `refClient` | string | no | Client Reference request body field documented by the smsmode API. |
| `callbackUrlStatus` | string | no | Status Callback URL request body field documented by the smsmode API. |
| `callbackUrlMo` | string | no | MO Callback URL request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrlMo": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "endDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "refClient": "string",
      "sentDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrlMo` | string |  |
| `callbackUrlStatus` | string |  |
| `endDate` | date |  |
| `name` | string |  |
| `refClient` | string |  |
| `sentDate` | date |  |

## Native endpoint

Through the native smsmode API, this operation is `PATCH rcs/v1/channels/:channelId/campaigns/:campaignId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-rcs-campaign.md) for the provider-specific parameters and requirements.

