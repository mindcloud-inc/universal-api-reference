# ClinicalTrials.gov: Get Enums



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-enums
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-enums?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-enums?${params}`, {
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
      "pieces": [
        "string"
      ],
      "type": "string",
      "values": [
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
| `pieces` | array<string> | ClinicalTrials.gov pieces using this enum. |
| `type` | string | Enumeration type name. |
| `values` | array<object> | Allowed enum values and legacy labels. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /studies/enums` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enums.md) for the provider-specific parameters and requirements.

