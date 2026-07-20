# FEMA: List Hazard Mitigation Assistance Projects

Retrieves hazard mitigation assistance projects from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hazard-mitigation-assistance-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hazard-mitigation-assistance-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hazard-mitigation-assistance-projects?${params}`, {
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
      "benefitCostRatio": 1,
      "costSharePercentage": 1,
      "county": "string",
      "countyCode": "string",
      "dataSource": "string",
      "dateApproved": "2026-05-07T12:00:00.000Z",
      "dateClosed": "2026-05-07T12:00:00.000Z",
      "dateInitiallyApproved": "2026-05-07T12:00:00.000Z",
      "disasterNumber": 1,
      "federalShareObligated": 1,
      "id": "string",
      "initialObligationAmount": 1,
      "initialObligationDate": "2026-05-07T12:00:00.000Z",
      "netValueBenefits": 1,
      "numberOfFinalProperties": 1,
      "numberOfProperties": 1,
      "programArea": "string",
      "programFy": 1,
      "projectAmount": 1,
      "projectCounties": "string",
      "projectIdentifier": "string",
      "projectType": "string",
      "recipient": "string",
      "recipientAdminCostAmt": 1,
      "recipientTribalIndicator": true,
      "region": 1,
      "srmcObligatedAmt": 1,
      "state": "string",
      "stateNumberCode": "string",
      "status": "string",
      "subrecipient": "string",
      "subrecipientAdminCostAmt": 1,
      "subrecipientTribalIndicator": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `benefitCostRatio` | number |  |
| `costSharePercentage` | number |  |
| `county` | string |  |
| `countyCode` | string |  |
| `dataSource` | string |  |
| `dateApproved` | date |  |
| `dateClosed` | date |  |
| `dateInitiallyApproved` | date |  |
| `disasterNumber` | number |  |
| `federalShareObligated` | number |  |
| `id` | string |  |
| `initialObligationAmount` | number |  |
| `initialObligationDate` | date |  |
| `netValueBenefits` | number |  |
| `numberOfFinalProperties` | number |  |
| `numberOfProperties` | number |  |
| `programArea` | string |  |
| `programFy` | number |  |
| `projectAmount` | number |  |
| `projectCounties` | string |  |
| `projectIdentifier` | string |  |
| `projectType` | string |  |
| `recipient` | string |  |
| `recipientAdminCostAmt` | number |  |
| `recipientTribalIndicator` | boolean |  |
| `region` | number |  |
| `srmcObligatedAmt` | number |  |
| `state` | string |  |
| `stateNumberCode` | string |  |
| `status` | string |  |
| `subrecipient` | string |  |
| `subrecipientAdminCostAmt` | number |  |
| `subrecipientTribalIndicator` | boolean |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v4/HazardMitigationAssistanceProjects` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hazard-mitigation-assistance-projects.md) for the provider-specific parameters and requirements.

