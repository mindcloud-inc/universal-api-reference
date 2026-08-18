# Centerpoint: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-contacts?${params}`, {
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
      "attributes": {
        "allProperties": true,
        "companyId": 1,
        "companyName": "Ava Chen",
        "createdAt": "string",
        "deletedAt": {},
        "email": {},
        "externalId": "string",
        "fax": {},
        "groupId": 1,
        "imageId": {},
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
        "position": "string",
        "propertyCount": 1,
        "recentActivity": {},
        "roles": "string",
        "timezone": "string",
        "updatedAt": "string",
        "userRoleId": {}
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
| `attributes.deletedAt` | object |  |
| `attributes.email` | object |  |
| `attributes.externalId` | string |  |
| `attributes.fax` | object |  |
| `attributes.groupId` | number |  |
| `attributes.imageId` | object |  |
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
| `attributes.position` | string |  |
| `attributes.propertyCount` | number |  |
| `attributes.recentActivity` | object |  |
| `attributes.roles` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.userRoleId` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET profiles` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

