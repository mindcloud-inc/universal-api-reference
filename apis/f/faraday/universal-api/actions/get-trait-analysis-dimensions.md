# Faraday: Get Trait Analysis Dimensions

Retrieves trait analysis dimensions from Faraday.

```
GET https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-trait-analysis-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-trait-analysis-dimensions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-trait-analysis-dimensions?${params}`, {
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
| `trait_id` | string | no | Faraday trait ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bins": [
        {}
      ],
      "traitName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bins` | array<object> | Analysis bins. |
| `traitName` | string | Trait name used in the analysis. |

## Native endpoint

Through the native Faraday API, this operation is `GET /traits/:trait_id/analysis/dimensions` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trait-analysis-dimensions.md) for the provider-specific parameters and requirements.

