# Rillion Prime: List Roles



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-roles?${params}`, {
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
| `user` | string | no | Optional user login name to scope the role list. Example: `AdminUser`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "authorizationAmount": 1,
      "authorizationOutstandingAmountBelow": {},
      "authorizationOutstandingAmountExceed": {},
      "authorizationOutstandingAmountPercentBelow": {},
      "authorizationOutstandingAmountPercentExceed": {},
      "chTime": {},
      "chUser": {},
      "defaultAddressId": {},
      "defaultCompany": {},
      "defaultObject1Id": {},
      "defaultObject2Id": {},
      "defaultObject3Id": {},
      "defaultObject4Id": {},
      "defaultObject5Id": {},
      "defaultObject6Id": {},
      "defaultObject7Id": {},
      "defaultObject8Id": {},
      "flowProposalId": {},
      "forProcessing": {},
      "forwardSupervisor": {},
      "group1": {},
      "group2": {},
      "group3": {},
      "headersOnly": {},
      "includableInFlow": {},
      "keyValuesRowState": {},
      "locked": true,
      "lockedRowId": {},
      "lockedRowLoginName": {},
      "lockedRowRole": {},
      "name": {},
      "newAuthorizationAmount": {},
      "newAuthorizationAmountDateTime": {},
      "newAuthorizationAmountRole": {},
      "newAuthorizationAmountUser": {},
      "permissionGroupBitCode": {},
      "powerRole": {},
      "reminderArrival": {},
      "reminderDueDate": {},
      "reminderImmidiateBitCode": {},
      "reminderSupervisor": {},
      "role": "string",
      "roleAdministrator": {},
      "roleCompanies": [
        "string"
      ],
      "roleSupervisor": {},
      "roleUserEmails": {},
      "roleUserLogins": {},
      "roleUserNames": [
        "Ava Chen"
      ],
      "rowState": {},
      "selectAccount": {},
      "selectCommodity": {},
      "selectCompany": {},
      "selected": {},
      "selectExpenseType": {},
      "selectObject1": {},
      "selectObject2": {},
      "selectObject3": {},
      "selectObject4": {},
      "selectObject5": {},
      "selectObject6": {},
      "selectObject7": {},
      "selectObject8": {},
      "userGroup": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `authorizationAmount` | number |  |
| `authorizationOutstandingAmountBelow` | object |  |
| `authorizationOutstandingAmountExceed` | object |  |
| `authorizationOutstandingAmountPercentBelow` | object |  |
| `authorizationOutstandingAmountPercentExceed` | object |  |
| `chTime` | object |  |
| `chUser` | object |  |
| `defaultAddressId` | object |  |
| `defaultCompany` | object |  |
| `defaultObject1Id` | object |  |
| `defaultObject2Id` | object |  |
| `defaultObject3Id` | object |  |
| `defaultObject4Id` | object |  |
| `defaultObject5Id` | object |  |
| `defaultObject6Id` | object |  |
| `defaultObject7Id` | object |  |
| `defaultObject8Id` | object |  |
| `flowProposalId` | object |  |
| `forProcessing` | object |  |
| `forwardSupervisor` | object |  |
| `group1` | object |  |
| `group2` | object |  |
| `group3` | object |  |
| `headersOnly` | object |  |
| `includableInFlow` | object |  |
| `keyValuesRowState` | object |  |
| `locked` | boolean |  |
| `lockedRowId` | object |  |
| `lockedRowLoginName` | object |  |
| `lockedRowRole` | object |  |
| `name` | object |  |
| `newAuthorizationAmount` | object |  |
| `newAuthorizationAmountDateTime` | object |  |
| `newAuthorizationAmountRole` | object |  |
| `newAuthorizationAmountUser` | object |  |
| `permissionGroupBitCode` | object |  |
| `powerRole` | object |  |
| `reminderArrival` | object |  |
| `reminderDueDate` | object |  |
| `reminderImmidiateBitCode` | object |  |
| `reminderSupervisor` | object |  |
| `role` | string |  |
| `roleAdministrator` | object |  |
| `roleCompanies[]` | string |  |
| `roleSupervisor` | object |  |
| `roleUserEmails` | object |  |
| `roleUserLogins` | object |  |
| `roleUserNames[]` | string |  |
| `rowState` | object |  |
| `selectAccount` | object |  |
| `selectCommodity` | object |  |
| `selectCompany` | object |  |
| `selected` | object |  |
| `selectExpenseType` | object |  |
| `selectObject1` | object |  |
| `selectObject2` | object |  |
| `selectObject3` | object |  |
| `selectObject4` | object |  |
| `selectObject5` | object |  |
| `selectObject6` | object |  |
| `selectObject7` | object |  |
| `selectObject8` | object |  |
| `userGroup` | object |  |

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /role` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

