# DealMachine: Add Lead



```
POST https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/add-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DealMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/add-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/add-lead', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Street address for the lead when using parsed address input. |
| `address2` | string | no | Optional second address line when using parsed address input. |
| `city` | string | no | City for the lead when using parsed address input. |
| `state` | string | no | State for the lead when using parsed address input. |
| `zip` | string | no | ZIP code for the lead when using parsed address input. |
| `latitude` | number | no | Latitude for the lead when using coordinate input. |
| `longitude` | number | no | Longitude for the lead when using coordinate input. |
| `fullAddress` | string | no | Single-string full address for the lead when using full-address input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {
        "label": "string",
        "value": 1
      },
      "buildingSquareFeet": 1,
      "campaignStatus": {
        "label": "string"
      },
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "equityAmount": 1,
      "equityPercent": "string",
      "estimatedRepairCost": 1,
      "estimatedValue": 1,
      "hasEmailAddress": true,
      "hasPhoneNumber": true,
      "id": 1,
      "isVacant": true,
      "leadSource": "string",
      "leadStatus": {
        "label": "string",
        "value": 1
      },
      "listingAgentEmail": "ava@example.com",
      "listingAgentName": "Ava Chen",
      "listingAgentPhone": "string",
      "lists": [
        {
          "id": "string",
          "label": "string",
          "listType": "string",
          "title": "string",
          "value": "string"
        }
      ],
      "mailDesign": {
        "label": "string"
      },
      "mailSequence": {
        "label": "string"
      },
      "marketStatus": {
        "label": "string",
        "value": "string"
      },
      "matchedLead": true,
      "mortgageAmount": 1,
      "numberOfStackedLists": 1,
      "owner1Name": "Ava Chen",
      "owner2Name": "Ava Chen",
      "ownerAddressFull": "string",
      "ownerLocation": "string",
      "ownerType": "string",
      "propertyAddressCity": "string",
      "propertyAddressFull": "string",
      "propertyAddressLine1": "string",
      "propertyAddressState": "string",
      "propertyAddressZipcode": "string",
      "propertyLatitude": "string",
      "propertyLongitude": "string",
      "propertyType": {
        "label": "string",
        "value": "string"
      },
      "saleDate": "2026-05-07T12:00:00.000Z",
      "salePrice": 1,
      "totalBaths": "string",
      "uniqueOwnerType": "string",
      "yearBuilt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo.label` | string |  |
| `assignedTo.value` | number |  |
| `buildingSquareFeet` | number |  |
| `campaignStatus.label` | string |  |
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `equityAmount` | number |  |
| `equityPercent` | string |  |
| `estimatedRepairCost` | number |  |
| `estimatedValue` | number |  |
| `hasEmailAddress` | boolean |  |
| `hasPhoneNumber` | boolean |  |
| `id` | number |  |
| `isVacant` | boolean |  |
| `leadSource` | string |  |
| `leadStatus.label` | string |  |
| `leadStatus.value` | number |  |
| `listingAgentEmail` | string |  |
| `listingAgentName` | string |  |
| `listingAgentPhone` | string |  |
| `lists[].id` | string |  |
| `lists[].label` | string |  |
| `lists[].listType` | string |  |
| `lists[].title` | string |  |
| `lists[].value` | string |  |
| `mailDesign.label` | string |  |
| `mailSequence.label` | string |  |
| `marketStatus.label` | string |  |
| `marketStatus.value` | string |  |
| `matchedLead` | boolean |  |
| `mortgageAmount` | number |  |
| `numberOfStackedLists` | number |  |
| `owner1Name` | string |  |
| `owner2Name` | string |  |
| `ownerAddressFull` | string |  |
| `ownerLocation` | string |  |
| `ownerType` | string |  |
| `propertyAddressCity` | string |  |
| `propertyAddressFull` | string |  |
| `propertyAddressLine1` | string |  |
| `propertyAddressState` | string |  |
| `propertyAddressZipcode` | string |  |
| `propertyLatitude` | string |  |
| `propertyLongitude` | string |  |
| `propertyType.label` | string |  |
| `propertyType.value` | string |  |
| `saleDate` | date |  |
| `salePrice` | number |  |
| `totalBaths` | string |  |
| `uniqueOwnerType` | string |  |
| `yearBuilt` | string |  |

## Native endpoint

Through the native DealMachine API, this operation is `POST /public/v1/leads/` (base URL `https://api.dealmachine.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-lead.md) for the provider-specific parameters and requirements.

