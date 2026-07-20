# ClickSend SMS: List SMS History

Retrieves SMS history from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-history?${params}`, {
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
| `q` | string | no | Search query for SMS history records. |
| `dateFrom` | string | no | Lower bound date filter for history. |
| `dateTo` | string | no | Upper bound date filter for history. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Sort directive supported by ClickSend history endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "apiUsername": "Ava Chen",
          "body": "string",
          "carrier": "string",
          "contactId": {},
          "country": "string",
          "customString": "string",
          "date": 1,
          "direction": "string",
          "errorCode": {},
          "errorText": {},
          "firstName": {},
          "from": "string",
          "fromEmail": {},
          "lastName": {},
          "listId": {},
          "messageId": "string",
          "messageParts": 1,
          "messagePrice": "string",
          "schedule": "string",
          "status": "string",
          "statusCode": {},
          "statusText": {},
          "subaccountId": 1,
          "to": "string",
          "userId": 1
        }
      ],
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].apiUsername` | string |  |
| `data[].body` | string |  |
| `data[].carrier` | string |  |
| `data[].contactId` | object |  |
| `data[].country` | string |  |
| `data[].customString` | string |  |
| `data[].date` | number |  |
| `data[].direction` | string |  |
| `data[].errorCode` | object |  |
| `data[].errorText` | object |  |
| `data[].firstName` | object |  |
| `data[].from` | string |  |
| `data[].fromEmail` | object |  |
| `data[].lastName` | object |  |
| `data[].listId` | object |  |
| `data[].messageId` | string |  |
| `data[].messageParts` | number |  |
| `data[].messagePrice` | string |  |
| `data[].schedule` | string |  |
| `data[].status` | string |  |
| `data[].statusCode` | object |  |
| `data[].statusText` | object |  |
| `data[].subaccountId` | number |  |
| `data[].to` | string |  |
| `data[].userId` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/sms/history` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sms-history.md) for the provider-specific parameters and requirements.

