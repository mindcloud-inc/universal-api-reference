# Statsig: Delete Ingestion Source

Deletes an ingestion source from Statsig.

```
DELETE https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-ingestion-source-delete-console-v1-ingestion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-ingestion-source-delete-console-v1-ingestion?connectionId=$CONNECTION_ID&type=string&dataset=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string",
  "dataset": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-ingestion-source-delete-console-v1-ingestion?${params}`, {
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
| `type` | string | yes |  |
| `dataset` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `DELETE /console/v1/ingestion` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ingestion-source-delete-console-v1-ingestion.md) for the provider-specific parameters and requirements.

