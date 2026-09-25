# Microsoft Entra Universal API Examples

These examples use the MindCloud API key and Microsoft Entra connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations



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

Example response:

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

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftEntra/latest/actions/list-organizations).

## Create Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen",
  "mailEnabled": true,
  "mailNickname": "Ava Chen",
  "securityEnabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen",
    "mailEnabled": true,
    "mailNickname": "Ava Chen",
    "securityEnabled": true
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "deletedDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "expirationDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isAssignableToRole": true,
      "mail": "ava@example.com",
      "mailEnabled": true,
      "mailNickname": "Ava Chen",
      "membershipRule": "string",
      "membershipRuleProcessingState": "string",
      "onPremisesDomainName": "Ava Chen",
      "onPremisesLastSyncDateTime": "2026-05-07T12:00:00.000Z",
      "onPremisesNetBiosName": "Ava Chen",
      "onPremisesSamAccountName": "Ava Chen",
      "onPremisesSecurityIdentifier": "string",
      "onPremisesSyncEnabled": true,
      "preferredDataLocation": "string",
      "preferredLanguage": "string",
      "renewedDateTime": "2026-05-07T12:00:00.000Z",
      "securityEnabled": true,
      "securityIdentifier": "string",
      "theme": "string",
      "uniqueName": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Group action reference](actions/create-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftEntra/latest/actions/create-group).
