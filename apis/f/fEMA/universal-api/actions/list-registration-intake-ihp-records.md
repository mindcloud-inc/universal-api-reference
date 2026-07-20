# FEMA: List Registration Intake IHP Records

Retrieves registration intake IHP records from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-registration-intake-ihp-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-registration-intake-ihp-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-registration-intake-ihp-records?${params}`, {
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
      "city": "string",
      "county": "string",
      "disasterNumber": 1,
      "haAmount": 1,
      "haEligible": 1,
      "haReferrals": 1,
      "id": "string",
      "ihpAmount": 1,
      "ihpEligible": 1,
      "ihpReferrals": 1,
      "onaAmount": 1,
      "onaEligible": 1,
      "onaReferrals": 1,
      "state": "string",
      "totalValidRegistrations": 1,
      "validCallCenterRegistrations": 1,
      "validMobileRegistrations": 1,
      "validWebRegistrations": 1,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `county` | string |  |
| `disasterNumber` | number |  |
| `haAmount` | number |  |
| `haEligible` | number |  |
| `haReferrals` | number |  |
| `id` | string |  |
| `ihpAmount` | number |  |
| `ihpEligible` | number |  |
| `ihpReferrals` | number |  |
| `onaAmount` | number |  |
| `onaEligible` | number |  |
| `onaReferrals` | number |  |
| `state` | string |  |
| `totalValidRegistrations` | number |  |
| `validCallCenterRegistrations` | number |  |
| `validMobileRegistrations` | number |  |
| `validWebRegistrations` | number |  |
| `zipCode` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/RegistrationIntakeIndividualsHouseholdPrograms` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-registration-intake-ihp-records.md) for the provider-specific parameters and requirements.

