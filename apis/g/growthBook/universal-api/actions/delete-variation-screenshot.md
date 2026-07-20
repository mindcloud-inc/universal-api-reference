# GrowthBook: Delete a variation screenshot

Deletes a variation screenshot from GrowthBook.

```
DELETE https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-variation-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-variation-screenshot?connectionId=$CONNECTION_ID&id=prj_19g6smo332up7&variationId=0&path=sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prj_19g6smo332up7",
  "variationId": "0",
  "path": "sample"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-variation-screenshot?${params}`, {
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
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `variationId` | string | yes | Default: `0`. |
| `path` | string | yes | The screenshot path/URL to delete (from upload response) Default: `sample`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrowthBook API returns.

## Native endpoint

Through the native GrowthBook API, this operation is `DELETE /experiments/:id/variation/:variationId/screenshot` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-variation-screenshot.md) for the provider-specific parameters and requirements.

