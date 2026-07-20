# Meisterplan: Update Resource

Updates an existing resource in Meisterplan.

```
PUT https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes |  |
| `resourceKey` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `externalId` | string | no |  |
| `emailAddress` | string | no |  |
| `postalAddress` | object | no |  |
| `employmentPeriod` | object | no |  |
| `externalResource` | boolean | no |  |
| `primaryRole` | object | no |  |
| `calendar` | object | no |  |
| `obsUnits` | object | no |  |
| `skills[]` | array<string> | no |  |
| `resourceManager` | object | no |  |
| `costPerHour` | number | no |  |
| `costPerHourValidFrom` | date | no |  |
| `costRates[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendar": {
        "id": "string",
        "path": "string"
      },
      "costPerHour": 1,
      "emailAddress": "ava@example.com",
      "employmentPeriod": {
        "startDate": "2026-05-07T12:00:00.000Z",
        "terminationDate": "2026-05-07T12:00:00.000Z"
      },
      "externalId": "string",
      "externalResource": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "postalAddress": {
        "city": "string",
        "country": "string",
        "postalCode": "string"
      },
      "resourceKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar.id` | string | Calendar ID |
| `calendar.path` | string | Calendar path |
| `costPerHour` | number | Cost per hour |
| `emailAddress` | string | Email address |
| `employmentPeriod.startDate` | date | Employment start date |
| `employmentPeriod.terminationDate` | date | Employment termination date |
| `externalId` | string | External ID |
| `externalResource` | boolean | External resource flag |
| `firstName` | string | First name |
| `id` | string | Resource ID |
| `lastName` | string | Last name |
| `postalAddress.city` | string | Postal city |
| `postalAddress.country` | string | Postal country |
| `postalAddress.postalCode` | string | Postal code |
| `resourceKey` | string | Resource key |

## Native endpoint

Through the native Meisterplan API, this operation is `PATCH /resources/:resourceId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource.md) for the provider-specific parameters and requirements.

