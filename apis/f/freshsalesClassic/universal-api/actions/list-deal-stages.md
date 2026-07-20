# Freshsales Classic: List Deal Stages

Retrieves deal stages from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-deal-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-deal-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-deal-stages?${params}`, {
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
      "choiceType": 1,
      "dealPipelineId": 1,
      "forecastType": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "probability": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choiceType` | number | Freshsales internal choice type. |
| `dealPipelineId` | number | Parent deal pipeline ID. |
| `forecastType` | string | Forecast classification. |
| `id` | number | Deal stage ID. |
| `name` | string | Deal stage name. |
| `position` | number | Stage position. |
| `probability` | number | Stage probability percentage. |
| `updatedAt` | string | Last updated timestamp. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /selector/deal_stages` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-stages.md) for the provider-specific parameters and requirements.

