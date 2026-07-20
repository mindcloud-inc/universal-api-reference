# FEMA: List IHP Valid Registrations

Retrieves IHP valid registrations from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-ihp-valid-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-ihp-valid-registrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-ihp-valid-registrations?${params}`, {
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
      "applicantAge": "string",
      "appliedDate": "2026-05-07T12:00:00.000Z",
      "censusGeoid": "string",
      "county": "string",
      "damagedCity": "string",
      "damagedStateAbbreviation": "string",
      "damagedZipCode": "string",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "disasterNumber": 1,
      "emergencyNeeds": true,
      "fips": "string",
      "floodInsurance": true,
      "foodNeed": true,
      "grossIncome": "string",
      "haEligible": true,
      "haReferral": true,
      "homeDamage": true,
      "homeOwnersInsurance": true,
      "householdComposition": "string",
      "id": 1,
      "ihpAmount": 1,
      "ihpEligible": true,
      "ihpReferral": true,
      "incidentTypeCode": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "onaAmount": 1,
      "onaEligible": true,
      "onaReferral": true,
      "ownRent": "string",
      "primaryResidence": true,
      "registrationMethod": "string",
      "residenceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantAge` | string |  |
| `appliedDate` | date |  |
| `censusGeoid` | string |  |
| `county` | string |  |
| `damagedCity` | string |  |
| `damagedStateAbbreviation` | string |  |
| `damagedZipCode` | string |  |
| `declarationDate` | date |  |
| `disasterNumber` | number |  |
| `emergencyNeeds` | boolean |  |
| `fips` | string |  |
| `floodInsurance` | boolean |  |
| `foodNeed` | boolean |  |
| `grossIncome` | string |  |
| `haEligible` | boolean |  |
| `haReferral` | boolean |  |
| `homeDamage` | boolean |  |
| `homeOwnersInsurance` | boolean |  |
| `householdComposition` | string |  |
| `id` | number |  |
| `ihpAmount` | number |  |
| `ihpEligible` | boolean |  |
| `ihpReferral` | boolean |  |
| `incidentTypeCode` | string |  |
| `lastRefresh` | date |  |
| `onaAmount` | number |  |
| `onaEligible` | boolean |  |
| `onaReferral` | boolean |  |
| `ownRent` | string |  |
| `primaryResidence` | boolean |  |
| `registrationMethod` | string |  |
| `residenceType` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/IndividualsAndHouseholdsProgramValidRegistrations` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ihp-valid-registrations.md) for the provider-specific parameters and requirements.

