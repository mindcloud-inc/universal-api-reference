# MyHR: List Employee Time Off Requests



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-time-off-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-time-off-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-time-off-requests?${params}`, {
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
      "companyTimeoffReason": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "label": "string",
        "object": "string",
        "pid": "string"
      },
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "employee": {
        "isPartial": true,
        "object": "string",
        "pid": "string"
      },
      "endDate": "string",
      "numHours": "string",
      "object": "string",
      "pid": "string",
      "startDate": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyTimeoffReason.dateCreation` | string |  |
| `companyTimeoffReason.dateLastAction` | string |  |
| `companyTimeoffReason.label` | string |  |
| `companyTimeoffReason.object` | string |  |
| `companyTimeoffReason.pid` | string |  |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `employee.isPartial` | boolean |  |
| `employee.object` | string |  |
| `employee.pid` | string |  |
| `endDate` | string |  |
| `numHours` | string |  |
| `object` | string |  |
| `pid` | string |  |
| `startDate` | string |  |
| `status` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employee_timeoff_requests` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-time-off-requests.md) for the provider-specific parameters and requirements.

