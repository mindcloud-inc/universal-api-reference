# Farmbrite Universal API Examples

These examples use the MindCloud API key and Farmbrite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List tasks

Retrieves a list of tasks from Farmbrite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tasks?${params}`, {
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
      "cached": true,
      "currentPage": 1,
      "data": [
        {
          "activitySeriesId": "string",
          "allDay": "string",
          "assignedToId": "string",
          "checklist": [
            "string"
          ],
          "collaboratorIds": [
            "string"
          ],
          "color": "string",
          "complete": true,
          "completedBy": "string",
          "completedOn": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "createdById": "string",
          "description": "string",
          "endTime": "string",
          "frequency": "string",
          "hoursSpent": "string",
          "id": "string",
          "keywords": "string",
          "latitude": "string",
          "longitude": "string",
          "nextOccurrenceId": "string",
          "period": "string",
          "priority": "string",
          "referenceId": "string",
          "referenceType": "string",
          "repeatOnComplete": true,
          "repeatUntil": "string",
          "sourceId": "string",
          "sourceType": "string",
          "startTime": "string",
          "status": "string",
          "teamId": "string",
          "title": "string",
          "todo": true,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

See the full [List tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/farmbrite/latest/actions/list-tasks).

## Create animal

Creates a new animal in Farmbrite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-animal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-animal', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "acquiredFromId": "string",
      "billOfSaleId": "string",
      "birthDate": "string",
      "birthWeight": "string",
      "bredDate": "string",
      "breed": "string",
      "breederId": "string",
      "breedingSourceId": "string",
      "breedingStatus": "string",
      "breedingStock": true,
      "coloring": "string",
      "conditionScore": "string",
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": "string",
      "daysToWean": "string",
      "deathDate": "string",
      "deceasedReason": "string",
      "description": "string",
      "donated": true,
      "donatedDate": "string",
      "donatedValue": "string",
      "dueDate": "string",
      "electronicId": "string",
      "environmentScore": "string",
      "estimatedValue": "string",
      "expectedMaturityDate": "string",
      "famacha": "string",
      "fatherId": "string",
      "feed": "string",
      "gender": "string",
      "groupId": "string",
      "groupQty": "string",
      "harvestLabel": "string",
      "harvestUnit": "string",
      "healthScore": "string",
      "height": "string",
      "id": "string",
      "internalId": "string",
      "isGroup": true,
      "isNeutered": true,
      "keywords": "string",
      "marketPrice": "string",
      "matureWeight": "string",
      "measurementDate": "string",
      "motherId": "string",
      "name": "Ava Chen",
      "onFeed": true,
      "otherTagColor": "string",
      "otherTagLocation": "string",
      "otherTagNumber": "string",
      "purchased": true,
      "purchaseDate": "string",
      "purchasedFromId": "string",
      "purchasePrice": "string",
      "recordAlert": "string",
      "registryNumber": "string",
      "retentionScore": "string",
      "saleDate": "string",
      "salePrice": "string",
      "soldTo": "string",
      "status": "string",
      "tagColor": "string",
      "tagLocation": "string",
      "tagNumber": "string",
      "tattooLeft": "string",
      "tattooRight": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "weanedDate": "string",
      "weight": "string",
      "wellnessScore": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create animal action reference](actions/create-animal.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/farmbrite/latest/actions/create-animal).
