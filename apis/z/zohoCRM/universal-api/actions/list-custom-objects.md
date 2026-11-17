# Zoho CRM: List Custom Objects



```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/list-custom-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/list-custom-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/list-custom-objects?${params}`, {
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
      "accessType": "string",
      "actualPluralLabel": "string",
      "actualSingularLabel": "string",
      "apiName": "Ava Chen",
      "apiSupported": true,
      "arguments": [
        "string"
      ],
      "businessCardFieldLimit": 1,
      "convertable": true,
      "creatable": true,
      "deletable": true,
      "editable": true,
      "feedsRequired": true,
      "generatedType": "string",
      "globalSearchSupported": true,
      "hasMoreProfiles": true,
      "id": "string",
      "isBlueprintSupported": true,
      "lookupable": true,
      "modifiedBy": {
        "id": "string",
        "name": "Ava Chen"
      },
      "modifiedTime": "string",
      "moduleName": "Ava Chen",
      "parentModule": {
        "apiName": "Ava Chen",
        "id": "string"
      },
      "pluralLabel": "string",
      "presenceSubMenu": true,
      "profileCount": 1,
      "profiles": [
        "string"
      ],
      "publicFieldsConfigured": true,
      "quickCreate": true,
      "recycleBinOnDelete": true,
      "sequenceNumber": 1,
      "showAsTab": true,
      "singularLabel": "string",
      "status": "string",
      "subformProperties": {
        "displayField": {
          "apiName": "Ava Chen",
          "id": "string"
        }
      },
      "subMenuAvailable": true,
      "trackCurrentData": true,
      "viewable": true,
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessType` | string |  |
| `actualPluralLabel` | string |  |
| `actualSingularLabel` | string |  |
| `apiName` | string |  |
| `apiSupported` | boolean |  |
| `arguments` | array |  |
| `businessCardFieldLimit` | number |  |
| `convertable` | boolean |  |
| `creatable` | boolean |  |
| `deletable` | boolean |  |
| `editable` | boolean |  |
| `feedsRequired` | boolean |  |
| `generatedType` | string |  |
| `globalSearchSupported` | boolean |  |
| `hasMoreProfiles` | boolean |  |
| `id` | string |  |
| `isBlueprintSupported` | boolean |  |
| `lookupable` | boolean |  |
| `modifiedBy` | object |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedTime` | string |  |
| `moduleName` | string |  |
| `parentModule` | object |  |
| `parentModule.apiName` | string |  |
| `parentModule.id` | string |  |
| `pluralLabel` | string |  |
| `presenceSubMenu` | boolean |  |
| `profileCount` | number |  |
| `profiles` | array |  |
| `publicFieldsConfigured` | boolean |  |
| `quickCreate` | boolean |  |
| `recycleBinOnDelete` | boolean |  |
| `sequenceNumber` | number |  |
| `showAsTab` | boolean |  |
| `singularLabel` | string |  |
| `status` | string |  |
| `subformProperties` | object |  |
| `subformProperties.displayField` | object |  |
| `subformProperties.displayField.apiName` | string |  |
| `subformProperties.displayField.id` | string |  |
| `subMenuAvailable` | boolean |  |
| `trackCurrentData` | boolean |  |
| `viewable` | boolean |  |
| `visibility` | number |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /settings/modules` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-objects.md) for the provider-specific parameters and requirements.

