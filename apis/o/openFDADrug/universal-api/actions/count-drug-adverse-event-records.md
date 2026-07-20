# openFDA Drug: Count Drug Adverse Event Records

Counts drug adverse event records in openFDA Drug by field.

```
GET https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/count-drug-adverse-event-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openFDA Drug `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/count-drug-adverse-event-records?connectionId=$CONNECTION_ID&count=patient.drug.medicinalproduct.exact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "patient.drug.medicinalproduct.exact"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/count-drug-adverse-event-records?${params}`, {
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
| `count` | string | yes | Field to count by. Use .exact for exact phrase buckets when OpenFDA requires it. Default: `patient.drug.medicinalproduct.exact`. |
| `search` | string | no | Optional OpenFDA search expression to filter records before counting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | OpenFDA count buckets with term and count values. |

## Native endpoint

Through the native openFDA Drug API, this operation is `GET /drug/event.json` (base URL `https://api.fda.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-drug-adverse-event-records.md) for the provider-specific parameters and requirements.

