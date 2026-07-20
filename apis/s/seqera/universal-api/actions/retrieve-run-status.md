# Seqera: Retrieve Run Status

Retrieves a workflow run status from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/retrieve-run-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/retrieve-run-status?connectionId=$CONNECTION_ID&run_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "run_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/retrieve-run-status?${params}`, {
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
| `run_id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seqera API returns.

## Native endpoint

Through the native Seqera API, this operation is `GET /ga4gh/wes/v1/runs/:run_id/status` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-run-status.md) for the provider-specific parameters and requirements.

