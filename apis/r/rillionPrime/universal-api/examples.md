# Rillion Prime Universal API Examples

These examples use the MindCloud API key and Rillion Prime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Roles



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

Example response:

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

See the full [List Roles action reference](actions/list-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rillionPrime/latest/actions/list-roles).

## Create Purchase Order Delivery Queue Records



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-purchase-order-delivery-queue-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-purchase-order-delivery-queue-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Purchase Order Delivery Queue Records action reference](actions/create-purchase-order-delivery-queue-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rillionPrime/latest/actions/create-purchase-order-delivery-queue-records).
