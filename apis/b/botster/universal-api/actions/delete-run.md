# Botster: Delete Run

Deletes an existing run from Botster.

```
DELETE https://connect.mindcloud.co/v1/universal/botster/latest/actions/delete-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botster/latest/actions/delete-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botster/latest/actions/delete-run?${params}`, {
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
| `runId` | string | yes | The Botster run UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "run": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the run delete request succeeded. |
| `run.id` | string | Unique Botster run identifier. |

## Native endpoint

Through the native Botster API, this operation is `DELETE /runs/:runId` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-run.md) for the provider-specific parameters and requirements.

