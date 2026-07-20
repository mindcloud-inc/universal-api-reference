# Availity: Get Professional Cost Estimate

Retrieves a professional cost estimate from Availity.

```
GET https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-professional-cost-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-professional-cost-estimate?connectionId=$CONNECTION_ID&id=efe8b6ab-e47d-4975-aa73-adda35311850" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "efe8b6ab-e47d-4975-aa73-adda35311850"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-professional-cost-estimate?${params}`, {
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
| `id` | string | yes | Unique response ID from the initial PCE 2.0 professional cost estimate request. Example: `efe8b6ab-e47d-4975-aa73-adda35311850`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDt` | date | Creation timestamp returned by Availity. |
| `id` | string | Patient cost estimate response identifier. |
| `result` | object | Completed professional cost estimate result details. |
| `status` | string | Processing or completion status. |

## Native endpoint

Through the native Availity API, this operation is `GET /availity/v2/patient-cost-estimates/prof/{id}` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-professional-cost-estimate.md) for the provider-specific parameters and requirements.

