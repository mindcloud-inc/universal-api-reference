# Tinybird: Delete Matching Data



```
DELETE https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/delete-matching-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/delete-matching-data?connectionId=$CONNECTION_ID&deleteCondition=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deleteCondition": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/delete-matching-data?${params}`, {
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
| `deleteCondition` | string | yes | Required SQL WHERE condition; no DELETE keyword |
| `dryRun` | boolean | no | When true, validate and report matching rows without deleting |
| `name` | string | yes | The data source name to target. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinybird API returns.

## Native endpoint

Through the native Tinybird API, this operation is `POST v0/datasources/:name/delete` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-matching-data.md) for the provider-specific parameters and requirements.

