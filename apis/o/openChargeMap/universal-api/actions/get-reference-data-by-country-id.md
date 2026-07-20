# Open Charge Map: Get Reference Data By Country ID



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-reference-data-by-country-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-reference-data-by-country-id?connectionId=$CONNECTION_ID&countryId=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryId": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-reference-data-by-country-id?${params}`, {
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
| `countryId` | string | yes | Optional numeric country ID filter for Open Charge Map reference data. Default: `2`. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ChargePoint": {},
      "ChargerTypes": [
        {}
      ],
      "CheckinStatusTypes": [
        {}
      ],
      "ConnectionTypes": [
        {}
      ],
      "Countries": [
        {}
      ],
      "CurrentTypes": [
        {}
      ],
      "Operators": [
        {}
      ],
      "StatusTypes": [
        {}
      ],
      "UsageTypes": [
        {}
      ],
      "UserCommentTypes": [
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
| `ChargePoint` | object |  |
| `ChargerTypes` | array<object> |  |
| `CheckinStatusTypes` | array<object> |  |
| `ConnectionTypes` | array<object> |  |
| `Countries` | array<object> |  |
| `CurrentTypes` | array<object> |  |
| `Operators` | array<object> |  |
| `StatusTypes` | array<object> |  |
| `UsageTypes` | array<object> |  |
| `UserCommentTypes` | array<object> |  |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /referencedata` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reference-data-by-country-id.md) for the provider-specific parameters and requirements.

