# ERPLY Books: Get Employees

Retrieves employee records from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-employees?${params}`, {
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
      "records": [
        {
          "code": "string",
          "drawerID": "string",
          "email": "ava@example.com",
          "employeeID": "string",
          "employeeName": "Ava Chen",
          "fax": "string",
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "id": 1,
          "lastModified": 1,
          "lastModifiedByUserName": "Ava Chen",
          "lastName": "Chen",
          "mobile": "string",
          "phone": "string",
          "pointsOfSale": "string",
          "userGroupID": "string",
          "userID": "string",
          "username": "Ava Chen",
          "warehouses": [
            {
              "id": 1
            }
          ]
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].code` | string |  |
| `records[].drawerID` | string |  |
| `records[].email` | string |  |
| `records[].employeeID` | string |  |
| `records[].employeeName` | string |  |
| `records[].fax` | string |  |
| `records[].firstName` | string |  |
| `records[].fullName` | string |  |
| `records[].id` | number |  |
| `records[].lastModified` | number |  |
| `records[].lastModifiedByUserName` | string |  |
| `records[].lastName` | string |  |
| `records[].mobile` | string |  |
| `records[].phone` | string |  |
| `records[].pointsOfSale` | string |  |
| `records[].userGroupID` | string |  |
| `records[].userID` | string |  |
| `records[].username` | string |  |
| `records[].warehouses[].id` | number |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employees.md) for the provider-specific parameters and requirements.

