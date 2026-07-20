# Farmbrite: Create animal

Creates a new animal in Farmbrite.

```
POST https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-animal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acquiredFromId` | string |  |
| `billOfSaleId` | string |  |
| `birthDate` | string |  |
| `birthWeight` | string |  |
| `bredDate` | string |  |
| `breed` | string |  |
| `breederId` | string |  |
| `breedingSourceId` | string |  |
| `breedingStatus` | string |  |
| `breedingStock` | boolean |  |
| `coloring` | string |  |
| `conditionScore` | string |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `customFields` | string |  |
| `daysToWean` | string |  |
| `deathDate` | string |  |
| `deceasedReason` | string |  |
| `description` | string |  |
| `donated` | boolean |  |
| `donatedDate` | string |  |
| `donatedValue` | string |  |
| `dueDate` | string |  |
| `electronicId` | string |  |
| `environmentScore` | string |  |
| `estimatedValue` | string |  |
| `expectedMaturityDate` | string |  |
| `famacha` | string |  |
| `fatherId` | string |  |
| `feed` | string |  |
| `gender` | string |  |
| `groupId` | string |  |
| `groupQty` | string |  |
| `harvestLabel` | string |  |
| `harvestUnit` | string |  |
| `healthScore` | string |  |
| `height` | string |  |
| `id` | string |  |
| `internalId` | string |  |
| `isGroup` | boolean |  |
| `isNeutered` | boolean |  |
| `keywords` | string |  |
| `marketPrice` | string |  |
| `matureWeight` | string |  |
| `measurementDate` | string |  |
| `motherId` | string |  |
| `name` | string |  |
| `onFeed` | boolean |  |
| `otherTagColor` | string |  |
| `otherTagLocation` | string |  |
| `otherTagNumber` | string |  |
| `purchased` | boolean |  |
| `purchaseDate` | string |  |
| `purchasedFromId` | string |  |
| `purchasePrice` | string |  |
| `recordAlert` | string |  |
| `registryNumber` | string |  |
| `retentionScore` | string |  |
| `saleDate` | string |  |
| `salePrice` | string |  |
| `soldTo` | string |  |
| `status` | string |  |
| `tagColor` | string |  |
| `tagLocation` | string |  |
| `tagNumber` | string |  |
| `tattooLeft` | string |  |
| `tattooRight` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `weanedDate` | string |  |
| `weight` | string |  |
| `wellnessScore` | string |  |

## Native endpoint

Through the native Farmbrite API, this operation is `POST /animals` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-animal.md) for the provider-specific parameters and requirements.

