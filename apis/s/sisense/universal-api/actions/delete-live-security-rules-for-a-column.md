# Sisense: Delete Live Security Rules For A Column

Deletes live security rules for a Sisense column.

```
DELETE https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-live-security-rules-for-a-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-live-security-rules-for-a-column?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-live-security-rules-for-a-column?${params}`, {
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
| `column` | string | no | The column name. |
| `table` | string | no | The table name. |
| `title` | string | no | The live Datamodel title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `DELETE /api/v1/elasticubes/live/:title/datasecurity/:table/:column` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-live-security-rules-for-a-column.md) for the provider-specific parameters and requirements.

