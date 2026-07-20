# Meisterplan: Delete Program

Deletes an existing program from Meisterplan.

```
DELETE https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-program?connectionId=$CONNECTION_ID&scenarioId=string&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "string",
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-program?${params}`, {
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
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `programId` | string | yes | Internal Meisterplan program identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Meisterplan API returns.

## Native endpoint

Through the native Meisterplan API, this operation is `DELETE /scenarios/:scenarioId/programs/:programId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-program.md) for the provider-specific parameters and requirements.

