# Microsoft Entra: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-organizations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated organization properties to return. Example: `id,displayName,verifiedDomains`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedPlans": [
        {
          "assignedDateTime": "2026-05-07T12:00:00.000Z",
          "capabilityStatus": "string",
          "service": "string",
          "servicePlanId": "string"
        }
      ],
      "businessPhones": [
        "string"
      ],
      "city": "string",
      "country": "string",
      "countryLetterCode": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "defaultUsageLocation": "string",
      "deletedDateTime": "2026-05-07T12:00:00.000Z",
      "directorySizeQuota": {
        "total": 1,
        "used": 1
      },
      "displayName": "Ava Chen",
      "id": "string",
      "isMultipleDataLocationsForServicesEnabled": true,
      "onPremisesLastSyncDateTime": "2026-05-07T12:00:00.000Z",
      "onPremisesSyncEnabled": true,
      "partnerTenantType": "string",
      "postalCode": "string",
      "preferredLanguage": "string",
      "privacyProfile": {},
      "provisionedPlans": [
        {
          "capabilityStatus": "string",
          "provisioningStatus": "string",
          "service": "string"
        }
      ],
      "state": "string",
      "street": "string",
      "technicalNotificationMails": [
        "ava@example.com"
      ],
      "tenantType": "string",
      "verifiedDomains": [
        {
          "capabilities": "string",
          "isDefault": true,
          "isInitial": true,
          "name": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedPlans[].assignedDateTime` | date |  |
| `assignedPlans[].capabilityStatus` | string |  |
| `assignedPlans[].service` | string |  |
| `assignedPlans[].servicePlanId` | string |  |
| `businessPhones[]` | string |  |
| `city` | string |  |
| `country` | string |  |
| `countryLetterCode` | string |  |
| `createdDateTime` | date |  |
| `defaultUsageLocation` | string |  |
| `deletedDateTime` | date |  |
| `directorySizeQuota.total` | number |  |
| `directorySizeQuota.used` | number |  |
| `displayName` | string |  |
| `id` | string |  |
| `isMultipleDataLocationsForServicesEnabled` | boolean |  |
| `onPremisesLastSyncDateTime` | date |  |
| `onPremisesSyncEnabled` | boolean |  |
| `partnerTenantType` | string |  |
| `postalCode` | string |  |
| `preferredLanguage` | string |  |
| `privacyProfile` | object |  |
| `provisionedPlans[].capabilityStatus` | string |  |
| `provisionedPlans[].provisioningStatus` | string |  |
| `provisionedPlans[].service` | string |  |
| `state` | string |  |
| `street` | string |  |
| `technicalNotificationMails[]` | string |  |
| `tenantType` | string |  |
| `verifiedDomains[].capabilities` | string |  |
| `verifiedDomains[].isDefault` | boolean |  |
| `verifiedDomains[].isInitial` | boolean |  |
| `verifiedDomains[].name` | string |  |
| `verifiedDomains[].type` | string |  |

## Native endpoint

Through the native Microsoft Entra API, this operation is `GET /organization` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

