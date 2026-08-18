# Create Contact with Centerpoint

## Endpoint

- **Method:** `POST`
- **Path:** `profiles`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create Contact](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/profilesPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adjustablePermissions.timekeepingUpdate` | body | `boolean` | no | — |
| `lists.accountManagers` | body | `boolean` | no | — |
| `name` | body | `string` | yes | — |
| `options.truckId` | body | `string` | no | — |
| `adjustablePermissions.drawingsPricingUpdate` | body | `boolean` | no | — |
| `companyId` | body | `number` | no | — |
| `lists.projectManagers` | body | `boolean` | no | — |
| `options.laborCost` | body | `number` | no | — |
| `adjustablePermissions.accountDownload` | body | `boolean` | no | — |
| `lists.serviceHelpers` | body | `boolean` | no | — |
| `options.propertyIDs[]` | body | `array<number>` | no | — |
| `userId` | body | `number` | no | — |
| `lists.technicians` | body | `boolean` | no | — |
| `options.serviceNotifications` | body | `object` | no | — |
| `userRoleId` | body | `number` | no | — |
| `groupId` | body | `number` | no | — |
| `options.serviceNotificationsProperty` | body | `object` | no | — |
| `externalId` | body | `string` | no | — |
| `options.serviceNotificationsCompany` | body | `object` | no | — |
| `importId` | body | `string` | no | — |
| `options.serviceNotificationsTexas` | body | `object` | no | — |
| `email` | body | `string` | no | — |
| `options.serviceNotificationsNonTexas` | body | `object` | no | — |
| `options.serviceNotificationsCorporate` | body | `object` | no | — |
| `position` | body | `string` | no | — |
| `office` | body | `string` | no | Main office phone number |
| `options.serviceNotificationsNonCorporate` | body | `object` | no | — |
| `officeExt` | body | `string` | no | Main office phone number extension |
| `options.productionNotifications` | body | `object` | no | — |
| `mobile` | body | `string` | no | — |
| `options.productionNotificationsCorporate` | body | `object` | no | — |
| `fax` | body | `string` | no | — |
| `options.productionNotificationsNonCorporate` | body | `object` | no | — |
| `imageID` | body | `string` | no | — |
| `options.productionNotificationsCompany` | body | `object` | no | — |
| `isActive` | body | `boolean` | no | — |
| `options.productionNotificationsProperty` | body | `object` | no | — |
| `allProperties` | body | `boolean` | no | — |
| `options.allowedFileLibraryTags[]` | body | `array<string>` | no | — |
| `isBilling` | body | `boolean` | no | — |
| `options.allowedMenuItems[]` | body | `array<string>` | no | — |
| `options` | body | `object` | no | — |
| `options.emailSignature` | body | `string` | no | — |
| `timezone` | body | `list` | no | — |
| `lists` | body | `object` | no | — |
| `adjustablePermissions` | body | `object` | no | — |
| `custom` | body | `object` | no | — |
