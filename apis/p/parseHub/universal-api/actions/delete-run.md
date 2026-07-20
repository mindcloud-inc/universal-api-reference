# ParseHub: Delete Run



```
DELETE https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/delete-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ParseHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/delete-run?connectionId=$CONNECTION_ID&runToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/delete-run?${params}`, {
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
| `runToken` | string | yes | The ParseHub token of the run to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "runToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `runToken` | string | The ParseHub run token that was deleted. |

## Native endpoint

Through the native ParseHub API, this operation is `DELETE /runs/{run_token}` (base URL `https://www.parsehub.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-run.md) for the provider-specific parameters and requirements.

