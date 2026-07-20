# Freshsales Classic: List All Deals

Retrieves deals from a Freshsales Classic view.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-deals?connectionId=$CONNECTION_ID&viewId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-deals?${params}`, {
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
| `page` | number | no | Page number to return for the selected deal view. |
| `viewId` | number | yes | The deal view ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "amount": "string",
      "closedDate": "string",
      "dealPipelineId": 1,
      "dealStageId": 1,
      "expectedClose": "string",
      "expectedDealValue": "string",
      "forecastCategory": 1,
      "hasProducts": true,
      "id": 1,
      "name": "Ava Chen",
      "probability": 1,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `amount` | string |  |
| `closedDate` | string |  |
| `dealPipelineId` | number |  |
| `dealStageId` | number |  |
| `expectedClose` | string |  |
| `expectedDealValue` | string |  |
| `forecastCategory` | number |  |
| `hasProducts` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `probability` | number |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /deals/view/:viewId` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-deals.md) for the provider-specific parameters and requirements.

