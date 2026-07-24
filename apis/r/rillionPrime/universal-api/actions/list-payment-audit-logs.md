# Rillion Prime Pay: List Payment Audit Logs



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&searchReferenceId=RillionPay2&referenceType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchReferenceId": "RillionPay2",
  "referenceType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-audit-logs?${params}`, {
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
| `searchReferenceId` | string | yes | Reference ID to search for in payment audit logs. Example: `RillionPay2`. |
| `referenceType` | list<string> | yes | Reference type to search for in payment audit logs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auditLogs": [
        {
          "data": [
            {
              "action": "string",
              "date": "string",
              "details": "string",
              "newState": "string",
              "previousState": {},
              "username": "Ava Chen"
            }
          ],
          "referenceId": "string",
          "totalPages": 1,
          "totalRecords": 1
        }
      ],
      "pageIndex": 1,
      "pageSize": 1,
      "referenceType": "string",
      "searchReferenceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditLogs[].data[].action` | string |  |
| `auditLogs[].data[].date` | string |  |
| `auditLogs[].data[].details` | string |  |
| `auditLogs[].data[].newState` | string |  |
| `auditLogs[].data[].previousState` | object |  |
| `auditLogs[].data[].username` | string |  |
| `auditLogs[].referenceId` | string |  |
| `auditLogs[].totalPages` | number |  |
| `auditLogs[].totalRecords` | number |  |
| `pageIndex` | number |  |
| `pageSize` | number |  |
| `referenceType` | string |  |
| `searchReferenceId` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/audit` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-audit-logs.md) for the provider-specific parameters and requirements.

