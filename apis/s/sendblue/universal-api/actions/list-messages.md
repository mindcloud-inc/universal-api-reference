# Sendblue: List Messages

Retrieves a list of messages from Sendblue.

```
GET https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/list-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountEmail` | string | no | Filter by account email. Example: `mindcloud`. |
| `createdAtGte` | date | no | Only include messages created at or after this ISO 8601 timestamp. Example: `2026-03-13T00:00:00.000Z`. |
| `createdAtLte` | date | no | Only include messages created at or before this ISO 8601 timestamp. Example: `2026-03-13T23:59:59.999Z`. |
| `fromNumber` | string | no | Filter by sending number. Example: `+16232843671`. |
| `groupId` | string | no | Filter by group ID. Example: `sb_group_123`. |
| `isOutbound` | boolean | no | Filter outbound vs inbound messages. |
| `messageType` | string | no | Filter by message type. Example: `message`. |
| `number` | string | no | Filter by recipient number. Example: `+584248435662`. |
| `sendblueNumber` | string | no | Filter by Sendblue number. Example: `+16232843671`. |
| `sentAtGte` | date | no | Only include messages sent at or after this ISO 8601 timestamp. Example: `2026-03-13T00:00:00.000Z`. |
| `sentAtLte` | date | no | Only include messages sent at or before this ISO 8601 timestamp. Example: `2026-03-13T23:59:59.999Z`. |
| `service` | string | no | Filter by service. Example: `iMessage`. |
| `status` | string | no | Filter by delivery status. Example: `DELIVERED`. |
| `toNumber` | string | no | Filter by to-number. Example: `+584248435662`. |
| `updatedAtGte` | date | no | Only include messages updated at or after this ISO 8601 timestamp. Example: `2026-03-13T00:00:00.000Z`. |
| `updatedAtLte` | date | no | Only include messages updated at or before this ISO 8601 timestamp. Example: `2026-03-13T23:59:59.999Z`. |
| `workerId` | string | no | Filter by worker ID. Example: `worker_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "accountEmail": "ava@example.com",
          "content": "string",
          "dateSent": "string",
          "dateUpdated": "string",
          "errorCode": 1,
          "errorDetail": "string",
          "errorMessage": "string",
          "errorReason": "string",
          "fromNumber": "string",
          "groupDisplayName": {},
          "groupId": "string",
          "isOutbound": true,
          "mediaUrl": "https://example.com",
          "messageHandle": "string",
          "messageType": "string",
          "optedOut": true,
          "plan": "string",
          "sendblueNumber": {},
          "sendStyle": "string",
          "service": {},
          "status": "string",
          "wasDowngraded": {}
        }
      ],
      "pagination": {
        "hasMore": true,
        "limit": 1,
        "offset": 1,
        "total": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].accountEmail` | string |  |
| `data[].content` | string |  |
| `data[].dateSent` | string |  |
| `data[].dateUpdated` | string |  |
| `data[].errorCode` | number |  |
| `data[].errorDetail` | string |  |
| `data[].errorMessage` | string |  |
| `data[].errorReason` | string |  |
| `data[].fromNumber` | string |  |
| `data[].groupDisplayName` | object |  |
| `data[].groupId` | string |  |
| `data[].isOutbound` | boolean |  |
| `data[].mediaUrl` | string |  |
| `data[].messageHandle` | string |  |
| `data[].messageType` | string |  |
| `data[].optedOut` | boolean |  |
| `data[].plan` | string |  |
| `data[].sendblueNumber` | object |  |
| `data[].sendStyle` | string |  |
| `data[].service` | object |  |
| `data[].status` | string |  |
| `data[].wasDowngraded` | object |  |
| `pagination.hasMore` | boolean |  |
| `pagination.limit` | number |  |
| `pagination.offset` | number |  |
| `pagination.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `GET /api/v2/messages` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

