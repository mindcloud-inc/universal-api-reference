# HubSpot: Update Contact by ID

Updates an existing contact in HubSpot.

```
PUT https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-contact-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-contact-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Contact ID to update. |
| `properties.firstname` | string | no |  |
| `properties` | object | yes | Properties object to update. |
| `properties.lastname` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "id": "string",
      "properties": {
        "closedate": "string",
        "createdate": "string",
        "daysToClose": "string",
        "firstDealCreatedDate": "string",
        "firstname": "Ava",
        "hsAllAccessibleTeamIds": "string",
        "hsAllOwnerIds": "string",
        "hsAllTeamIds": "string",
        "hsCountIsUnworked": "string",
        "hsCountIsWorked": "string",
        "hsIsUnworked": "string",
        "hsObjectId": "string",
        "hsObjectSource": "string",
        "hsObjectSourceId": "string",
        "hsObjectSourceLabel": "string",
        "hsPipeline": "string",
        "hsTimeBetweenContactCreationAndDealClose": "string",
        "hsTimeBetweenContactCreationAndDealCreation": "string",
        "hsTimeToFirstEngagement": "string",
        "hsUpdatedByUserId": "string",
        "hsUserIdsOfAllOwners": "string",
        "hsV2DateEnteredCurrentStage": "string",
        "hsV2DateEnteredCustomer": "string",
        "hsV2TimeInCurrentStage": "string",
        "hubspotOwnerAssigneddate": "string",
        "hubspotOwnerId": "string",
        "hubspotTeamId": "string",
        "lastmodifieddate": "string",
        "lastname": "Chen",
        "lifecyclestage": "string",
        "notesLastUpdated": "string"
      },
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `id` | string |  |
| `properties.closedate` | string |  |
| `properties.createdate` | string |  |
| `properties.daysToClose` | string |  |
| `properties.firstDealCreatedDate` | string |  |
| `properties.firstname` | string |  |
| `properties.hsAllAccessibleTeamIds` | string |  |
| `properties.hsAllOwnerIds` | string |  |
| `properties.hsAllTeamIds` | string |  |
| `properties.hsCountIsUnworked` | string |  |
| `properties.hsCountIsWorked` | string |  |
| `properties.hsIsUnworked` | string |  |
| `properties.hsObjectId` | string |  |
| `properties.hsObjectSource` | string |  |
| `properties.hsObjectSourceId` | string |  |
| `properties.hsObjectSourceLabel` | string |  |
| `properties.hsPipeline` | string |  |
| `properties.hsTimeBetweenContactCreationAndDealClose` | string |  |
| `properties.hsTimeBetweenContactCreationAndDealCreation` | string |  |
| `properties.hsTimeToFirstEngagement` | string |  |
| `properties.hsUpdatedByUserId` | string |  |
| `properties.hsUserIdsOfAllOwners` | string |  |
| `properties.hsV2DateEnteredCurrentStage` | string |  |
| `properties.hsV2DateEnteredCustomer` | string |  |
| `properties.hsV2TimeInCurrentStage` | string |  |
| `properties.hubspotOwnerAssigneddate` | string |  |
| `properties.hubspotOwnerId` | string |  |
| `properties.hubspotTeamId` | string |  |
| `properties.lastmodifieddate` | string |  |
| `properties.lastname` | string |  |
| `properties.lifecyclestage` | string |  |
| `properties.notesLastUpdated` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `PATCH crm/v3/objects/contacts/:contactId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-by-id.md) for the provider-specific parameters and requirements.

