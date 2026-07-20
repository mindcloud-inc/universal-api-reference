# IntakeQ: Query Claims

Retrieves claims from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-claims?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-claims?${params}`, {
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
      "diagnosis": [
        "string"
      ],
      "patientAccountNumber": "string",
      "patientFirstName": "Ava",
      "patientLastName": "Chen",
      "payerName": "Ava Chen",
      "procedures": [
        {}
      ],
      "providerFirstName": "Ava",
      "providerLastName": "Chen",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diagnosis` | array<string> |  |
| `patientAccountNumber` | string |  |
| `patientFirstName` | string |  |
| `patientLastName` | string |  |
| `payerName` | string |  |
| `procedures` | array<object> |  |
| `providerFirstName` | string |  |
| `providerLastName` | string |  |
| `status` | number |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /claims` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-claims.md) for the provider-specific parameters and requirements.

