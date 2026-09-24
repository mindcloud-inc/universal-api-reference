# EHS Insight: Update User Contact

Warning: This endpoint doesn't allow partial updates, you need to pass all values to avoid data loss

```
PUT https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/update-user-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/update-user-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rowUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/update-user-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rowUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rowUid` | string | yes | The provider RowUID of the user contact to update. |
| `changeToken` | string | no |  |
| `userContactNumber` | string | no |  |
| `userContactType` | string | no |  |
| `fullName` | string | no |  |
| `isEnabled` | number | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `gender` | string | no |  |
| `birthDate` | string | no | format example: "2026-04-28" |
| `businessEntity` | string | no |  |
| `employer` | string | no |  |
| `position` | string | no |  |
| `employeeId` | string | no |  |
| `hireDate` | string | no | format example: "2026-04-28" |
| `positionStartDate` | string | no | format example: "2026-04-28" |
| `industryStartDate` | string | no | format example: "2026-04-28" |
| `homeAddress` | string | no |  |
| `homeCity` | string | no |  |
| `homeState` | string | no |  |
| `homeZip` | string | no |  |
| `phoneNumber` | string | no |  |
| `Username` | string | no |  |
| `AuthProvider` | string | no |  |
| `EmailAddress` | string | no |  |
| `Supervisor` | string | no |  |
| `InviteSent` | number | no |  |
| `UserContactPhoto` | string | no |  |
| `UDFPersonalCellPhone` | string | no |  |
| `UDFEmploymentType` | string | no |  |
| `Udfcdl` | number | no |  |
| `UDFDriversLicense` | string | no |  |
| `UDFDriversLicenseExpira` | string | no | format example: "2026-04-28" |
| `UDFLCACellPhoneNumber` | string | no |  |
| `UDFOfficePhone` | string | no |  |
| `UDFTerminationDate` | string | no | format example: "2026-04-28" |
| `MobilePhoneNumber` | string | no |  |
| `UserContactPhotoAttachmentUID` | string | no |  |
| `UserContactPhotoContentType` | string | no |  |
| `UserContactPhotoFileSize` | string | no |  |
| `Language` | string | no |  |
| `LanguageOther` | string | no |  |
| `UIMode` | string | no |  |
| `UIModeOther` | string | no |  |
| `GenderOther` | string | no |  |
| `PositionOther` | string | no |  |
| `UDFEmploymentTypeOther` | string | no |  |
| `EmployerOther` | string | no |  |
| `AuthProviderOther` | string | no |  |
| `UserContactPhotoPreviousVersions[]` | array | no |  |
| `RoleAssignmentType` | string | no |  |
| `SecurityGroups[]` | array | no |  |
| `UserRoles[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `POST /v6/entity/UserContact/update` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-contact.md) for the provider-specific parameters and requirements.

