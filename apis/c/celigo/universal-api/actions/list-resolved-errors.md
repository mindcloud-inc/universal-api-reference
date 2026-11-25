# Celigo: List Resolved Errors



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-resolved-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-resolved-errors?connectionId=$CONNECTION_ID&flowId=string&stepId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string",
  "stepId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-resolved-errors?${params}`, {
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
| `flowId` | list<string> | yes | Flow that owns the step. |
| `stepId` | string | yes | Export or import ID of the flow step. Get it from Get Flow (pageGenerators / pageProcessors) or Get Flow Error Summary. |
| `resolvedAtGte` | date | no | Only return errors resolved at or after this time. Required when Flow Job ID is set. |
| `resolvedAtLte` | date | no | Only return errors resolved at or before this time. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `occurredAtGte` | date | no | Only return errors that originally occurred at or after this time. |
| `occurredAtLte` | date | no | Only return errors that originally occurred at or before this time. |
| `flowJobId` | string | no | Only return errors from this flow-run job. Must be sent with Resolved at or After. |
| `tags[]` | array<string> | no | Only return errors carrying at least one of these tag IDs. |
| `resolvedBy[]` | array<string> | no | Only return errors resolved by these user IDs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Celigo API returns.

## Native endpoint

Through the native Celigo API, this operation is `GET /flows/:flowId/:stepId/resolved` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resolved-errors.md) for the provider-specific parameters and requirements.

