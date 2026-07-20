# Coast: Get Person By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getperson
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getperson?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getperson?${params}`, {
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
| `personId` | string | yes | Coast person ID of the person to retrieve. |

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
          "noLocation": true,
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
| `access.locations.noLocation` | boolean |  |
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

Through the native Coast API, this operation is `GET /v2/people/:personId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getperson.md) for the provider-specific parameters and requirements.

