# Freshsales Classic: List Deal Pipelines

Retrieves deal pipelines from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-deal-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-deal-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-deal-pipelines?${params}`, {
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
      "aggregatedField": "string",
      "configs": [
        {}
      ],
      "dealStages": [
        {}
      ],
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "position": 1,
      "rottingDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregatedField` | string | Aggregated field used by the pipeline. |
| `configs` | array<object> | Pipeline board field configuration. |
| `dealStages` | array<object> | Stages contained in the pipeline. |
| `id` | number | Deal pipeline ID. |
| `isDefault` | boolean | Whether the pipeline is the default pipeline. |
| `name` | string | Deal pipeline name. |
| `position` | number | Pipeline position. |
| `rottingDays` | number | Rotting threshold in days. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /selector/deal_pipelines` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-pipelines.md) for the provider-specific parameters and requirements.

