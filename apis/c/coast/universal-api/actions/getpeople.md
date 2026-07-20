# Coast: Get All People



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpeople
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpeople?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpeople?${params}`, {
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
| `email` | string | no | Return responses with email |
| `nextPageToken` | string | no | A token that represents the next page of results. This token is returned in the response of a previous request and should be used to retrieve the next set of results. If not provided, the first page of results will be returned. |
| `phoneNumber` | string | no | Return results with matching phone number |
| `pageSize` | number | no | The maximum number of results to return per page. If this parameter is not specified, the page size will be 10. This parameter works in conjunction with pagination tokens. |
| `active` | boolean | no | Return responses with active state |
| `departmentId` | string | no | Only return people assigned to this Coast department ID. |
| `locationId` | string | no | Only return people assigned to this Coast location ID. |
| `policyId` | string | no | Only return people assigned to this Coast policy ID. |
| `roleId` | string | no | Only return people assigned to this Coast role ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {
        "departments": {
          "noDepartment": true,
          "type": "string"
        },
        "locations": {
          "type": "string"
        },
        "type": "string"
      },
      "accountId": "string",
      "active": true,
      "arePurchasesLocked": true,
      "assignedVehicleId": {},
      "createdTime": "string",
      "departmentDetails": {},
      "departmentId": {},
      "email": "ava@example.com",
      "externalId": {},
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "locationDetails": {},
      "locationId": {},
      "mobilePhone": "string",
      "policyDetails": {
        "name": "Ava Chen"
      },
      "policyId": "string",
      "roleDetails": {
        "name": "Ava Chen"
      },
      "roleId": "string",
      "security": {
        "enableSmsSecurity": true,
        "pin": {},
        "smsSecurityMethod": "string"
      },
      "updatedTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access.departments.noDepartment` | boolean |  |
| `access.departments.type` | string |  |
| `access.locations.type` | string |  |
| `access.type` | string |  |
| `accountId` | string |  |
| `active` | boolean |  |
| `arePurchasesLocked` | boolean |  |
| `assignedVehicleId` | object |  |
| `createdTime` | string |  |
| `departmentDetails` | object |  |
| `departmentId` | object |  |
| `email` | string |  |
| `externalId` | object |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `locationDetails` | object |  |
| `locationId` | object |  |
| `mobilePhone` | string |  |
| `policyDetails.name` | string |  |
| `policyId` | string |  |
| `roleDetails.name` | string |  |
| `roleId` | string |  |
| `security.enableSmsSecurity` | boolean |  |
| `security.pin` | object |  |
| `security.smsSecurityMethod` | string |  |
| `updatedTime` | string |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/people` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/getpeople.md) for the provider-specific parameters and requirements.

