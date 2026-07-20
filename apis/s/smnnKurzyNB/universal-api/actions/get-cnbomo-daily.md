# Směnné kurzy ČNB: Get CNB OMO Daily

Retrieves the last valid OMO data from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnbomo-daily
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnbomo-daily?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnbomo-daily?${params}`, {
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
| `date` | date | no | Example: `2026-04-14`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "operations": [
        {
          "allotmentPercentage": 1,
          "averageAllotedRateInPercent": 1,
          "averageBidRateInPercent": 1,
          "liquidityImpact": "string",
          "marginalRateInPercent": 1,
          "maturityDate": "string",
          "maximumAllotedRateInPercent": 1,
          "maximumBidRateInPercent": 1,
          "minimumAllotedRateInPercent": 1,
          "minimumBidRateInPercent": 1,
          "operationType": "string",
          "settlementDate": "string",
          "totalAllotedVolumeInCZKbln": 1,
          "totalBidVolumeInCZKbln": 1,
          "totalNumberOfAllotedBids": 1,
          "totalNumberOfBids": 1,
          "tradeDate": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `operations[].allotmentPercentage` | number |  |
| `operations[].averageAllotedRateInPercent` | number |  |
| `operations[].averageBidRateInPercent` | number |  |
| `operations[].liquidityImpact` | string |  |
| `operations[].marginalRateInPercent` | number |  |
| `operations[].maturityDate` | string |  |
| `operations[].maximumAllotedRateInPercent` | number |  |
| `operations[].maximumBidRateInPercent` | number |  |
| `operations[].minimumAllotedRateInPercent` | number |  |
| `operations[].minimumBidRateInPercent` | number |  |
| `operations[].operationType` | string |  |
| `operations[].settlementDate` | string |  |
| `operations[].totalAllotedVolumeInCZKbln` | number |  |
| `operations[].totalBidVolumeInCZKbln` | number |  |
| `operations[].totalNumberOfAllotedBids` | number |  |
| `operations[].totalNumberOfBids` | number |  |
| `operations[].tradeDate` | string |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /omo/daily` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnbomo-daily.md) for the provider-specific parameters and requirements.

