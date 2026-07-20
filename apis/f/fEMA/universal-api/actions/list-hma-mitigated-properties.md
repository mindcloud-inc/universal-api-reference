# FEMA: List HMA Mitigated Properties

Retrieves HMA mitigated properties from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-mitigated-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-mitigated-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-mitigated-properties?${params}`, {
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
      "actualAmountPaid": 1,
      "city": "string",
      "county": "string",
      "damageCategory": "string",
      "disasterNumber": 1,
      "foundationType": "string",
      "id": "string",
      "numberOfProperties": 1,
      "programArea": "string",
      "programFy": 1,
      "projectIdentifier": "string",
      "propertyAction": "string",
      "propertyPartOfProject": "string",
      "region": 1,
      "state": "string",
      "stateNumberCode": "string",
      "structureType": "string",
      "typeOfResidency": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualAmountPaid` | number |  |
| `city` | string |  |
| `county` | string |  |
| `damageCategory` | string |  |
| `disasterNumber` | number |  |
| `foundationType` | string |  |
| `id` | string |  |
| `numberOfProperties` | number |  |
| `programArea` | string |  |
| `programFy` | number |  |
| `projectIdentifier` | string |  |
| `propertyAction` | string |  |
| `propertyPartOfProject` | string |  |
| `region` | number |  |
| `state` | string |  |
| `stateNumberCode` | string |  |
| `structureType` | string |  |
| `typeOfResidency` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v4/HazardMitigationAssistanceMitigatedProperties` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hma-mitigated-properties.md) for the provider-specific parameters and requirements.

