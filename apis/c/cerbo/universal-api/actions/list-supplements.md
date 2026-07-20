# Cerbo: List Supplements

Retrieves supplement records from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-supplements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-supplements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-supplements?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active_only` | boolean | no | If this parameter is set it will only include ACTIVE supplements |
| `vendor_code` | string | no | If this parameter is set it will only supplements with matching vendor code (note, this is different from the external_ref_id). |
| `class` | string | no | If this parameter is set it will only supplements with that class specified |
| `external_ref_id` | string | no | If this parameter is set it will only include items with the designated external identifier - generally you will want to make this unique so it only includes a single item. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `GET /supplements` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-supplements.md) for the provider-specific parameters and requirements.

