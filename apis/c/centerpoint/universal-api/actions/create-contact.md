# Centerpoint: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adjustablePermissions.timekeepingUpdate` | boolean | no |  |
| `lists.accountManagers` | boolean | no |  |
| `name` | string | yes |  |
| `options.truckID` | string | no |  |
| `adjustablePermissions.drawingsPricingUpdate` | boolean | no |  |
| `companyID` | number | no |  |
| `lists.projectManagers` | boolean | no |  |
| `options.laborCost` | number | no |  |
| `adjustablePermissions.accountDownload` | boolean | no |  |
| `lists.serviceHelpers` | boolean | no |  |
| `options.propertyIDs[]` | array<number> | no |  |
| `userID` | number | no |  |
| `lists.technicians` | boolean | no |  |
| `options.serviceNotifications` | object | no |  |
| `userRoleID` | number | no |  |
| `groupID` | number | no |  |
| `options.serviceNotificationsProperty` | object | no |  |
| `options.serviceNotificationsCompany` | object | no |  |
| `options.serviceNotificationsTexas` | object | no |  |
| `email` | string | no |  |
| `options.serviceNotificationsNonTexas` | object | no |  |
| `options.serviceNotificationsCorporate` | object | no |  |
| `office` | string | no | Main office phone number |
| `options.serviceNotificationsNonCorporate` | object | no |  |
| `officeExt` | string | no | Main office phone number extension |
| `options.productionNotifications` | object | no |  |
| `mobile` | string | no |  |
| `options.productionNotificationsCorporate` | object | no |  |
| `options.productionNotificationsNonCorporate` | object | no |  |
| `options.productionNotificationsCompany` | object | no |  |
| `isActive` | boolean | no |  |
| `options.productionNotificationsProperty` | object | no |  |
| `options.allowedFileLibraryTags[]` | array<string> | no |  |
| `isBilling` | boolean | no |  |
| `options.allowedMenuItems[]` | array<string> | no |  |
| `options.emailSignature` | string | no |  |
| `timezone` | list | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalID` | string | no |  |
| `importID` | string | no |  |
| `position` | string | no |  |
| `fax` | string | no |  |
| `imageID` | string | no |  |
| `allProperties` | boolean | no |  |
| `options` | object | no |  |
| `lists` | object | no |  |
| `adjustablePermissions` | object | no |  |
| `custom` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `POST profiles` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

