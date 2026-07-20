# HubSpot: List Forms

Retrieves forms from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-forms?${params}`, {
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
| `limit` | number | no | Maximum number of forms to return. |
| `offset` | number | no | Pagination offset for forms. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "alwaysCreateNewCompany": true,
      "businessUnitId": 1,
      "campaignGuid": "string",
      "captchaEnabled": true,
      "captchaVersion": "string",
      "cloneable": true,
      "createdAt": 1,
      "createMarketableContact": true,
      "cssClass": "string",
      "customUid": "string",
      "deletable": true,
      "deletedAt": 1,
      "editable": true,
      "editVersion": 1,
      "embedVersion": "string",
      "enrichable": true,
      "followUpId": "string",
      "formFieldGroups": [
        [
          {}
        ]
      ],
      "formType": "string",
      "guid": "string",
      "ignoreCurrentValues": true,
      "inlineMessage": "string",
      "internalUpdatedAt": 1,
      "isPublished": true,
      "leadNurturingCampaignId": "string",
      "metaData": [
        [
          {}
        ]
      ],
      "method": "string",
      "migratedFrom": "string",
      "name": "Ava Chen",
      "notifyRecipients": "string",
      "parentId": 1,
      "performableHtml": "string",
      "portableKey": "string",
      "portalId": 1,
      "publishAt": 1,
      "publishedAt": 1,
      "redirect": "string",
      "selectedExternalOptions": [
        {
          "id": "string",
          "objectTypeId": "string",
          "propertyName": "Ava Chen",
          "referenceType": "string"
        }
      ],
      "spamNotificationsEnabled": true,
      "spamNotificationsRecipients": "string",
      "style": "string",
      "submitText": "string",
      "thankYouMessageJson": "string",
      "themeColor": "string",
      "themeName": "Ava Chen",
      "tmsId": "string",
      "unpublishAt": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `alwaysCreateNewCompany` | boolean |  |
| `businessUnitId` | number |  |
| `campaignGuid` | string |  |
| `captchaEnabled` | boolean |  |
| `captchaVersion` | string |  |
| `cloneable` | boolean |  |
| `createdAt` | number |  |
| `createMarketableContact` | boolean |  |
| `cssClass` | string |  |
| `customUid` | string |  |
| `deletable` | boolean |  |
| `deletedAt` | number |  |
| `editable` | boolean |  |
| `editVersion` | number |  |
| `embedVersion` | string |  |
| `enrichable` | boolean |  |
| `followUpId` | string |  |
| `formFieldGroups[]` | array<object> |  |
| `formFieldGroups[].default` | boolean |  |
| `formFieldGroups[].fields[]` | array<object> |  |
| `formFieldGroups[].fields[].defaultValue` | string |  |
| `formFieldGroups[].fields[].dependentFieldFilters[]` | array<string> |  |
| `formFieldGroups[].fields[].description` | string |  |
| `formFieldGroups[].fields[].displayOrder` | number |  |
| `formFieldGroups[].fields[].enabled` | boolean |  |
| `formFieldGroups[].fields[].fieldType` | string |  |
| `formFieldGroups[].fields[].groupName` | string |  |
| `formFieldGroups[].fields[].hidden` | boolean |  |
| `formFieldGroups[].fields[].isSmartField` | boolean |  |
| `formFieldGroups[].fields[].label` | string |  |
| `formFieldGroups[].fields[].labelHidden` | boolean |  |
| `formFieldGroups[].fields[].metaData[]` | array<string> |  |
| `formFieldGroups[].fields[].name` | string |  |
| `formFieldGroups[].fields[].objectTypeId` | string |  |
| `formFieldGroups[].fields[].options[]` | array<string> |  |
| `formFieldGroups[].fields[].placeholder` | string |  |
| `formFieldGroups[].fields[].propertyObjectType` | string |  |
| `formFieldGroups[].fields[].required` | boolean |  |
| `formFieldGroups[].fields[].selectedOptions[]` | array<string> |  |
| `formFieldGroups[].fields[].type` | string |  |
| `formFieldGroups[].fields[].unselectedLabel` | string |  |
| `formFieldGroups[].fields[].validation` | object |  |
| `formFieldGroups[].fields[].validation.blockedEmailAddresses[]` | array<string> |  |
| `formFieldGroups[].fields[].validation.checkPhoneFormat` | boolean |  |
| `formFieldGroups[].fields[].validation.data` | string |  |
| `formFieldGroups[].fields[].validation.message` | string |  |
| `formFieldGroups[].fields[].validation.name` | string |  |
| `formFieldGroups[].fields[].validation.useDefaultBlockList` | boolean |  |
| `formFieldGroups[].isPageBreak` | boolean |  |
| `formFieldGroups[].isSmartGroup` | boolean |  |
| `formFieldGroups[].richText` | object |  |
| `formFieldGroups[].richText.content` | string |  |
| `formFieldGroups[].richText.type` | string |  |
| `formType` | string |  |
| `guid` | string |  |
| `ignoreCurrentValues` | boolean |  |
| `inlineMessage` | string |  |
| `internalUpdatedAt` | number |  |
| `isPublished` | boolean |  |
| `leadNurturingCampaignId` | string |  |
| `metaData[]` | array<object> |  |
| `metaData[].name` | string |  |
| `metaData[].value` | string |  |
| `method` | string |  |
| `migratedFrom` | string |  |
| `name` | string |  |
| `notifyRecipients` | string |  |
| `parentId` | number |  |
| `performableHtml` | string |  |
| `portableKey` | string |  |
| `portalId` | number |  |
| `publishAt` | number |  |
| `publishedAt` | number |  |
| `redirect` | string |  |
| `selectedExternalOptions[]` | string |  |
| `selectedExternalOptions[].id` | string |  |
| `selectedExternalOptions[].objectTypeId` | string |  |
| `selectedExternalOptions[].propertyName` | string |  |
| `selectedExternalOptions[].referenceType` | string |  |
| `spamNotificationsEnabled` | boolean |  |
| `spamNotificationsRecipients` | string |  |
| `style` | string |  |
| `submitText` | string |  |
| `thankYouMessageJson` | string |  |
| `themeColor` | string |  |
| `themeName` | string |  |
| `tmsId` | string |  |
| `unpublishAt` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native HubSpot API, this operation is `GET forms/v2/forms` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

