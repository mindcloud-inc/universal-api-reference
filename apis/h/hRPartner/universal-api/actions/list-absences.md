# HR Partner: List Absences



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-absences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-absences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-absences?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "absenceDate": "2026-05-07T12:00:00.000Z",
      "absenceReason": "string",
      "absenceStatus": "string",
      "attachments": [
        {}
      ],
      "description": "string",
      "duration": 1,
      "employee": {},
      "id": 1,
      "leaveType": "string",
      "returnDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceDate` | date |  |
| `absenceReason` | string |  |
| `absenceStatus` | string |  |
| `attachments` | array<object> |  |
| `description` | string |  |
| `duration` | number |  |
| `employee` | object |  |
| `id` | number |  |
| `leaveType` | string |  |
| `returnDate` | date |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /absences` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-absences.md) for the provider-specific parameters and requirements.

