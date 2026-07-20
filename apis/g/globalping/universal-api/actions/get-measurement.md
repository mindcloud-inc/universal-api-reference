# Globalping: Get Measurement

Retrieves a Globalping measurement by ID.

```
GET https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-measurement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Globalping `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-measurement?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-measurement?${params}`, {
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
| `id` | string | yes | The measurement ID returned by a create measurement action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "probesCount": 1,
      "results": [
        {}
      ],
      "status": "string",
      "target": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | ISO timestamp when the measurement was created. |
| `id` | string | Measurement identifier. |
| `probesCount` | number | Number of probes assigned to the measurement. |
| `results` | array<object> | Per-probe measurement results. |
| `status` | string | Current measurement state. |
| `target` | string | Requested measurement target. |
| `type` | string | Measurement type. |
| `updatedAt` | string | ISO timestamp when the measurement was last updated. |

## Native endpoint

Through the native Globalping API, this operation is `GET /v1/measurements/:id` (base URL `https://api.globalping.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-measurement.md) for the provider-specific parameters and requirements.

