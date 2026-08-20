# Centerpoint: List Employees



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-employees?${params}`, {
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
| `fields[profiles]` | string | no | Optional fields profiles query parameter. |
| `fields[workTimeEntries]` | string | no | Optional fields work time entries query parameter. |
| `fields[employees]` | string | no | Optional fields employees query parameter. |
| `fields[productions]` | string | no | Optional fields productions query parameter. |
| `include` | string | no | Optional include query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "allProperties": true,
        "companyId": 1,
        "companyName": "Ava Chen",
        "createdAt": "string",
        "custom": {
          "primarycontactonsite": {}
        },
        "customWithLabels": {
          "primaryContactOnSite": {}
        },
        "deletedAt": {},
        "email": "ava@example.com",
        "externalId": "string",
        "fax": {},
        "groupId": 1,
        "imageId": 1,
        "importId": {},
        "isActive": true,
        "isBilling": true,
        "lastLoginAt": {},
        "mobile": {},
        "modules": {
          "betaTesting": true,
          "companies": true,
          "contacts": true,
          "contractors": true,
          "corporations": true,
          "cpAssist": true,
          "documents": true,
          "drawings": true,
          "dumpsters": true,
          "essentials": true,
          "estimates": true,
          "inspections": true,
          "interactiveProperty": true,
          "locations": true,
          "opportunities": true,
          "pictometryInEstimates": true,
          "productions": true,
          "properties": true,
          "proposals": true,
          "residential": true,
          "service": true,
          "serviceAgreements": true,
          "serviceEstimates": true,
          "tasks": true,
          "timekeeping": true,
          "timekeepingCostCodes": true,
          "vendors": true,
          "warranties": true
        },
        "name": "Ava Chen",
        "office": {},
        "officeExt": {},
        "options": {
          "productionNotifications": {
            "email": true,
            "sms": true
          },
          "productionNotificationsCompany": {
            "email": true,
            "sms": true
          },
          "productionNotificationsCorporate": {
            "email": true,
            "sms": true
          },
          "productionNotificationsNonCorporate": {
            "email": true,
            "sms": true
          },
          "productionNotificationsProperty": {
            "email": true,
            "sms": true
          },
          "propertyIds": [
            {}
          ],
          "serviceNotifications": {
            "email": true,
            "sms": true
          },
          "serviceNotificationsCompany": {
            "email": true,
            "sms": true
          },
          "serviceNotificationsCorporate": {
            "email": true,
            "sms": true
          },
          "serviceNotificationsNonCorporate": {
            "email": true,
            "sms": true
          },
          "serviceNotificationsNonTexas": {
            "email": true,
            "sms": true
          },
          "serviceNotificationsProperty": {
            "email": true,
            "sms": true
          },
          "serviceNotificationsTexas": {
            "email": true,
            "sms": true
          }
        },
        "position": {},
        "propertyCount": 1,
        "recentActivity": "string",
        "roles": "string",
        "timezone": "string",
        "updatedAt": "string",
        "userRoleId": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.allProperties` | boolean |  |
| `attributes.companyId` | number |  |
| `attributes.companyName` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.custom.primarycontactonsite` | object |  |
| `attributes.customWithLabels.primaryContactOnSite` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.email` | string |  |
| `attributes.externalId` | string |  |
| `attributes.fax` | object |  |
| `attributes.groupId` | number |  |
| `attributes.imageId` | number |  |
| `attributes.importId` | object |  |
| `attributes.isActive` | boolean |  |
| `attributes.isBilling` | boolean |  |
| `attributes.lastLoginAt` | object |  |
| `attributes.mobile` | object |  |
| `attributes.modules.betaTesting` | boolean |  |
| `attributes.modules.companies` | boolean |  |
| `attributes.modules.contacts` | boolean |  |
| `attributes.modules.contractors` | boolean |  |
| `attributes.modules.corporations` | boolean |  |
| `attributes.modules.cpAssist` | boolean |  |
| `attributes.modules.documents` | boolean |  |
| `attributes.modules.drawings` | boolean |  |
| `attributes.modules.dumpsters` | boolean |  |
| `attributes.modules.essentials` | boolean |  |
| `attributes.modules.estimates` | boolean |  |
| `attributes.modules.inspections` | boolean |  |
| `attributes.modules.interactiveProperty` | boolean |  |
| `attributes.modules.locations` | boolean |  |
| `attributes.modules.opportunities` | boolean |  |
| `attributes.modules.pictometryInEstimates` | boolean |  |
| `attributes.modules.productions` | boolean |  |
| `attributes.modules.properties` | boolean |  |
| `attributes.modules.proposals` | boolean |  |
| `attributes.modules.residential` | boolean |  |
| `attributes.modules.service` | boolean |  |
| `attributes.modules.serviceAgreements` | boolean |  |
| `attributes.modules.serviceEstimates` | boolean |  |
| `attributes.modules.tasks` | boolean |  |
| `attributes.modules.timekeeping` | boolean |  |
| `attributes.modules.timekeepingCostCodes` | boolean |  |
| `attributes.modules.vendors` | boolean |  |
| `attributes.modules.warranties` | boolean |  |
| `attributes.name` | string |  |
| `attributes.office` | object |  |
| `attributes.officeExt` | object |  |
| `attributes.options.productionNotifications.email` | boolean |  |
| `attributes.options.productionNotifications.sms` | boolean |  |
| `attributes.options.productionNotificationsCompany.email` | boolean |  |
| `attributes.options.productionNotificationsCompany.sms` | boolean |  |
| `attributes.options.productionNotificationsCorporate.email` | boolean |  |
| `attributes.options.productionNotificationsCorporate.sms` | boolean |  |
| `attributes.options.productionNotificationsNonCorporate.email` | boolean |  |
| `attributes.options.productionNotificationsNonCorporate.sms` | boolean |  |
| `attributes.options.productionNotificationsProperty.email` | boolean |  |
| `attributes.options.productionNotificationsProperty.sms` | boolean |  |
| `attributes.options.propertyIds` | array<object> |  |
| `attributes.options.serviceNotifications.email` | boolean |  |
| `attributes.options.serviceNotifications.sms` | boolean |  |
| `attributes.options.serviceNotificationsCompany.email` | boolean |  |
| `attributes.options.serviceNotificationsCompany.sms` | boolean |  |
| `attributes.options.serviceNotificationsCorporate.email` | boolean |  |
| `attributes.options.serviceNotificationsCorporate.sms` | boolean |  |
| `attributes.options.serviceNotificationsNonCorporate.email` | boolean |  |
| `attributes.options.serviceNotificationsNonCorporate.sms` | boolean |  |
| `attributes.options.serviceNotificationsNonTexas.email` | boolean |  |
| `attributes.options.serviceNotificationsNonTexas.sms` | boolean |  |
| `attributes.options.serviceNotificationsProperty.email` | boolean |  |
| `attributes.options.serviceNotificationsProperty.sms` | boolean |  |
| `attributes.options.serviceNotificationsTexas.email` | boolean |  |
| `attributes.options.serviceNotificationsTexas.sms` | boolean |  |
| `attributes.position` | object |  |
| `attributes.propertyCount` | number |  |
| `attributes.recentActivity` | string |  |
| `attributes.roles` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.userRoleId` | number |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET employees` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

