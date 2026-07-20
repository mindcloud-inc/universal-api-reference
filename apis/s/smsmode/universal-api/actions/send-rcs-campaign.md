# smsmode: Send RCS Campaign



```
POST https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/send-rcs-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/send-rcs-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "name": "Ava Chen",
  "recipients[]": [
    "string"
  ],
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/send-rcs-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "name": "Ava Chen",
    "recipients[]": ["string"],
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `name` | string | yes | Name request body field documented by the smsmode API. |
| `recipients[]` | array | yes | Recipients request body field documented by the smsmode API. |
| `body` | object | yes | Body request body field documented by the smsmode API. |
| `from` | string | no | Sender request body field documented by the smsmode API. |
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
      "body": {
        "type": "string"
      },
      "callbackUrlMo": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "endDate": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "name": "Ava Chen",
      "recipients": [
        {
          "refClient": "string",
          "to": "string"
        }
      ],
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
| `body.type` | string |  |
| `callbackUrlMo` | string |  |
| `callbackUrlStatus` | string |  |
| `endDate` | date |  |
| `from` | string |  |
| `name` | string |  |
| `recipients[].refClient` | string |  |
| `recipients[].to` | string |  |
| `refClient` | string |  |
| `sentDate` | date |  |

## Native endpoint

Through the native smsmode API, this operation is `POST rcs/v1/channels/:channelId/campaigns` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-rcs-campaign.md) for the provider-specific parameters and requirements.

