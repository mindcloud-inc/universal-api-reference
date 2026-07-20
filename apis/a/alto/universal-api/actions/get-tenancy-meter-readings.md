# Alto: Get Tenancy Meter Readings

Retrieves tenancy meter readings from Alto.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancy-meter-readings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancy-meter-readings?connectionId=$CONNECTION_ID&tenancyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenancyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancy-meter-readings?${params}`, {
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
| `tenancyId` | string | yes | Unique Alto tenancy identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "inValue": 1,
      "outValue": 1,
      "utilityType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `inValue` | number |  |
| `outValue` | number |  |
| `utilityType` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /tenancies/:tenancyId/meter-readings` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenancy-meter-readings.md) for the provider-specific parameters and requirements.

