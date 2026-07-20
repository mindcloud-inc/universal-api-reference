# FEMA: List Individual Assistance Housing Registrants

Retrieves individual assistance housing registrants from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-individual-assistance-housing-registrants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-individual-assistance-housing-registrants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-individual-assistance-housing-registrants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "censusBlockId": "string",
      "damagedCity": "string",
      "damagedStateAbbreviation": "string",
      "damagedZipCode": "string",
      "destroyed": true,
      "disasterNumber": 1,
      "floodDamage": true,
      "floodInsurance": true,
      "foundationDamage": true,
      "grossIncome": 1,
      "homeOwnersInsurance": true,
      "householdComposition": 1,
      "id": "string",
      "inspected": true,
      "ownRent": "string",
      "personalPropertyEligible": true,
      "primaryResidence": true,
      "rentalAssistanceEligible": true,
      "repairAssistanceEligible": true,
      "replacementAssistanceEligible": true,
      "residenceType": "string",
      "roofDamage": true,
      "specialNeeds": true,
      "tsaEligible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `censusBlockId` | string |  |
| `damagedCity` | string |  |
| `damagedStateAbbreviation` | string |  |
| `damagedZipCode` | string |  |
| `destroyed` | boolean |  |
| `disasterNumber` | number |  |
| `floodDamage` | boolean |  |
| `floodInsurance` | boolean |  |
| `foundationDamage` | boolean |  |
| `grossIncome` | number |  |
| `homeOwnersInsurance` | boolean |  |
| `householdComposition` | number |  |
| `id` | string |  |
| `inspected` | boolean |  |
| `ownRent` | string |  |
| `personalPropertyEligible` | boolean |  |
| `primaryResidence` | boolean |  |
| `rentalAssistanceEligible` | boolean |  |
| `repairAssistanceEligible` | boolean |  |
| `replacementAssistanceEligible` | boolean |  |
| `residenceType` | string |  |
| `roofDamage` | boolean |  |
| `specialNeeds` | boolean |  |
| `tsaEligible` | boolean |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/IndividualAssistanceHousingRegistrantsLargeDisasters` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-individual-assistance-housing-registrants.md) for the provider-specific parameters and requirements.

