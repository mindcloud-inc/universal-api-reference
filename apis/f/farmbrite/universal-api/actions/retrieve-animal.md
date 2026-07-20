# Farmbrite: Retrieve animal

Retrieves a specific animal from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-animal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-animal?connectionId=$CONNECTION_ID&animalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "animalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-animal?${params}`, {
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
| `animalId` | string | yes |  |

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

Through the native Farmbrite API, this operation is `GET /animals/:animal_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-animal.md) for the provider-specific parameters and requirements.

