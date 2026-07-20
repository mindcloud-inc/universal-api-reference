# DealMachine Universal API Examples

These examples use the MindCloud API key and DealMachine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lead Statuses



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-lead-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-lead-statuses?${params}`, {
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
      "id": 1,
      "label": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Lead Statuses action reference](actions/list-lead-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dealMachine/latest/actions/list-lead-statuses).

## Add Lead



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

Example response:

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

See the full [Add Lead action reference](actions/add-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dealMachine/latest/actions/add-lead).
