# Deputy: Get Leave Request

Retrieves a single leave request from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-leave-request?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-leave-request?${params}`, {
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
| `id` | number | yes | Leave request ID from Deputy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "AllDay": true,
      "Comment": "string",
      "Company": 1,
      "Created": "2026-05-07T12:00:00.000Z",
      "DateEnd": "2026-05-07T12:00:00.000Z",
      "DateStart": "2026-05-07T12:00:00.000Z",
      "Employee": 1,
      "EmployeeName": "Ava Chen",
      "End": 1,
      "EndTimeLocalized": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "LeaveRule": 1,
      "Modified": "2026-05-07T12:00:00.000Z",
      "Start": 1,
      "StartTimeLocalized": "2026-05-07T12:00:00.000Z",
      "Status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `AllDay` | boolean |  |
| `Comment` | string |  |
| `Company` | number |  |
| `Created` | date |  |
| `DateEnd` | date |  |
| `DateStart` | date |  |
| `Employee` | number |  |
| `EmployeeName` | string |  |
| `End` | number |  |
| `EndTimeLocalized` | date |  |
| `Id` | number |  |
| `LeaveRule` | number |  |
| `Modified` | date |  |
| `Start` | number |  |
| `StartTimeLocalized` | date |  |
| `Status` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v1/resource/Leave/:id` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-request.md) for the provider-specific parameters and requirements.

