# Farmbrite: List animals

Retrieves a list of animals from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-animals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-animals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-animals?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].acquiredFromId` | string |  |
| `data[].billOfSaleId` | string |  |
| `data[].birthDate` | string |  |
| `data[].birthWeight` | string |  |
| `data[].bredDate` | string |  |
| `data[].breed` | string |  |
| `data[].breederId` | string |  |
| `data[].breedingSourceId` | string |  |
| `data[].breedingStatus` | string |  |
| `data[].breedingStock` | boolean |  |
| `data[].coloring` | string |  |
| `data[].conditionScore` | string |  |
| `data[].contactId` | string |  |
| `data[].createdAt` | date |  |
| `data[].customFields` | string |  |
| `data[].daysToWean` | string |  |
| `data[].deathDate` | string |  |
| `data[].deceasedReason` | string |  |
| `data[].description` | string |  |
| `data[].donated` | boolean |  |
| `data[].donatedDate` | string |  |
| `data[].donatedValue` | string |  |
| `data[].dueDate` | string |  |
| `data[].electronicId` | string |  |
| `data[].environmentScore` | string |  |
| `data[].estimatedValue` | string |  |
| `data[].expectedMaturityDate` | string |  |
| `data[].famacha` | string |  |
| `data[].fatherId` | string |  |
| `data[].feed` | string |  |
| `data[].gender` | string |  |
| `data[].groupId` | string |  |
| `data[].groupQty` | string |  |
| `data[].harvestLabel` | string |  |
| `data[].harvestUnit` | string |  |
| `data[].healthScore` | string |  |
| `data[].height` | string |  |
| `data[].id` | string |  |
| `data[].internalId` | string |  |
| `data[].isGroup` | boolean |  |
| `data[].isNeutered` | boolean |  |
| `data[].keywords` | string |  |
| `data[].marketPrice` | string |  |
| `data[].matureWeight` | string |  |
| `data[].measurementDate` | string |  |
| `data[].motherId` | string |  |
| `data[].name` | string |  |
| `data[].onFeed` | boolean |  |
| `data[].otherTagColor` | string |  |
| `data[].otherTagLocation` | string |  |
| `data[].otherTagNumber` | string |  |
| `data[].purchased` | boolean |  |
| `data[].purchaseDate` | string |  |
| `data[].purchasedFromId` | string |  |
| `data[].purchasePrice` | string |  |
| `data[].recordAlert` | string |  |
| `data[].registryNumber` | string |  |
| `data[].retentionScore` | string |  |
| `data[].saleDate` | string |  |
| `data[].salePrice` | string |  |
| `data[].soldTo` | string |  |
| `data[].status` | string |  |
| `data[].tagColor` | string |  |
| `data[].tagLocation` | string |  |
| `data[].tagNumber` | string |  |
| `data[].tattooLeft` | string |  |
| `data[].tattooRight` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | date |  |
| `data[].weanedDate` | string |  |
| `data[].weight` | string |  |
| `data[].wellnessScore` | string |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /animals` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-animals.md) for the provider-specific parameters and requirements.

