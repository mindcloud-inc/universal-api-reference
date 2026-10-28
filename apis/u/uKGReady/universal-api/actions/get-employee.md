# UKG Ready: Get Employee



```
GET https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Ready `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/get-employee?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/get-employee?${params}`, {
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
| `companyID` | string | no |  |
| `accountID` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountExtraFields": [
        {
          "index": 1,
          "values": [
            {
              "value": "string"
            }
          ]
        }
      ],
      "address": {
        "addressLine1": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "zip": "string"
      },
      "addToNewHireExport": true,
      "costCentersInfo": {
        "defaults": [
          {
            "index": 1,
            "value": {
              "id": 1
            }
          }
        ]
      },
      "dates": {
        "birthday": "string",
        "hired": "string",
        "seniority": "string",
        "started": "string"
      },
      "ein": {
        "id": 1
      },
      "employeeId": "string",
      "firstName": "Ava",
      "firstScreen": {
        "id": "string"
      },
      "forceChangePassword": true,
      "id": 1,
      "lastName": "Chen",
      "Links": {
        "profiles": "https://example.com",
        "self": "https://example.com"
      },
      "locked": true,
      "managedCostCentersEnabled": true,
      "managers": [
        {
          "emplRef": {
            "accountId": 1
          },
          "index": 1
        }
      ],
      "nationalIdNumbers": [
        {
          "primary": true,
          "type": "string",
          "value": "string"
        }
      ],
      "phones": {
        "cellPhone": "string",
        "cellPhoneCountryCode": "string",
        "cellPhoneCountryId": "string",
        "preferredPhone": "string"
      },
      "primaryEmail": "ava@example.com",
      "secondaryEmail": "ava@example.com",
      "socialSecurity": "string",
      "status": "string",
      "timezone": "string",
      "username": "Ava Chen",
      "useSeparateMailingAddress": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountExtraFields[].index` | number |  |
| `accountExtraFields[].values[].value` | string |  |
| `address.addressLine1` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.state` | string |  |
| `address.zip` | string |  |
| `addToNewHireExport` | boolean |  |
| `costCentersInfo.defaults[].index` | number |  |
| `costCentersInfo.defaults[].value.id` | number |  |
| `dates.birthday` | string |  |
| `dates.hired` | string |  |
| `dates.seniority` | string |  |
| `dates.started` | string |  |
| `ein.id` | number |  |
| `employeeId` | string |  |
| `firstName` | string |  |
| `firstScreen.id` | string |  |
| `forceChangePassword` | boolean |  |
| `id` | number |  |
| `lastName` | string |  |
| `Links.profiles` | string |  |
| `Links.self` | string |  |
| `locked` | boolean |  |
| `managedCostCentersEnabled` | boolean |  |
| `managers[].emplRef.accountId` | number |  |
| `managers[].index` | number |  |
| `nationalIdNumbers[].primary` | boolean |  |
| `nationalIdNumbers[].type` | string |  |
| `nationalIdNumbers[].value` | string |  |
| `phones.cellPhone` | string |  |
| `phones.cellPhoneCountryCode` | string |  |
| `phones.cellPhoneCountryId` | string |  |
| `phones.preferredPhone` | string |  |
| `primaryEmail` | string |  |
| `secondaryEmail` | string |  |
| `socialSecurity` | string |  |
| `status` | string |  |
| `timezone` | string |  |
| `username` | string |  |
| `useSeparateMailingAddress` | boolean |  |

## Native endpoint

Through the native UKG Ready API, this operation is `GET /v2/companies/:cid/employees/:aid` (base URL `https://{{credentials.hostname}}/ta/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

