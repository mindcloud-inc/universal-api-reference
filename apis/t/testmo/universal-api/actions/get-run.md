# Testmo: Get Run

Retrieves run details from Testmo by ID.

```
GET https://connect.mindcloud.co/v1/universal/testmo/latest/actions/get-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/get-run?connectionId=$CONNECTION_ID&runId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testmo/latest/actions/get-run?${params}`, {
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
| `runId` | number | yes | ID of the run to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Testmo API returns.

## Native endpoint

Through the native Testmo API, this operation is `GET /runs/{run_id}` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run.md) for the provider-specific parameters and requirements.

