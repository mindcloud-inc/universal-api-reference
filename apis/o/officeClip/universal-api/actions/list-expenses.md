# OfficeClip: List Expenses

Retrieves expenses from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-expenses?${params}`, {
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
| `category` | string | yes | Required OfficeClip category such as inbox, outbox, or archived. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdByUserName": "Ava Chen",
          "currency": "string",
          "employeeId": "string",
          "fromDate": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "security": {
            "append": true,
            "delete": true,
            "read": true,
            "write": true
          },
          "stageId": 1,
          "status": "string",
          "toDate": "2026-05-07T12:00:00.000Z",
          "totalAmount": 1
        }
      ],
      "pagination": {
        "first": "string",
        "last": "string",
        "next": "string",
        "prev": "string",
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdByUserName` | string |  |
| `data[].currency` | string |  |
| `data[].employeeId` | string |  |
| `data[].fromDate` | date |  |
| `data[].id` | string |  |
| `data[].security.append` | boolean |  |
| `data[].security.delete` | boolean |  |
| `data[].security.read` | boolean |  |
| `data[].security.write` | boolean |  |
| `data[].stageId` | number |  |
| `data[].status` | string |  |
| `data[].toDate` | date |  |
| `data[].totalAmount` | number |  |
| `pagination.first` | string |  |
| `pagination.last` | string |  |
| `pagination.next` | string |  |
| `pagination.prev` | string |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/expense-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

