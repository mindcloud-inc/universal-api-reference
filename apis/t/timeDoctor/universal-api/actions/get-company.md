# Time Doctor: Get Company

Retrieves a company from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-company?${params}`, {
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
| `companyId` | string | yes | Company or workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allUsersTagId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "forceUserCount": 1,
      "hasManagedApprovals": true,
      "id": "string",
      "locked": true,
      "minBillableUsers": 1,
      "name": "Ava Chen",
      "oldCompanyId": "string",
      "pricingPlan": "string",
      "settings": {},
      "splitTest": [
        {}
      ],
      "subscription": {},
      "timezone": "string",
      "uniqueUserCount": 1,
      "userCount": 1,
      "userDiscount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allUsersTagId` | string |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `forceUserCount` | number |  |
| `hasManagedApprovals` | boolean |  |
| `id` | string |  |
| `locked` | boolean |  |
| `minBillableUsers` | number |  |
| `name` | string |  |
| `oldCompanyId` | string |  |
| `pricingPlan` | string |  |
| `settings` | object |  |
| `splitTest` | array<object> |  |
| `subscription` | object |  |
| `timezone` | string |  |
| `uniqueUserCount` | number |  |
| `userCount` | number |  |
| `userDiscount` | number |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/companies/:companyId` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

