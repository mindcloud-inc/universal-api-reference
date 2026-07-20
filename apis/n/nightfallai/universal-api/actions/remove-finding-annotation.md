# Nightfall.ai: Remove Finding Annotation

Deletes a finding annotation from Nightfall.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/remove-finding-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/remove-finding-annotation?connectionId=$CONNECTION_ID&findingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "findingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/remove-finding-annotation?${params}`, {
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
| `findingId` | string | yes | The UUID of the finding whose annotation should be removed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nightfall.ai API returns.

## Native endpoint

Through the native Nightfall.ai API, this operation is `POST /dlp/v1/findings/:findingId/unannotate` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-finding-annotation.md) for the provider-specific parameters and requirements.

