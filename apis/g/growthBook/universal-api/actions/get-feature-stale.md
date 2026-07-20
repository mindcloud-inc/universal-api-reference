# GrowthBook: Get stale status for one or more features

Retrieves stale status for GrowthBook features.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-stale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-stale?connectionId=$CONNECTION_ID&ids=sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "sample"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-stale?${params}`, {
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
| `ids` | string | yes | Comma-separated list of feature IDs (URL-encoded if needed). Example: `my_feature,another_feature` Default: `sample`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | object | Map of feature ID to stale status. Only requested features that were found and readable are included. |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /stale-features` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-stale.md) for the provider-specific parameters and requirements.

