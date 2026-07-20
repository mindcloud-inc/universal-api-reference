# Resco Cloud: List Questionnaire Results

Retrieves questionnaire results from Resco Cloud.

```
GET https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/list-questionnaire-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resco Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/list-questionnaire-results?connectionId=$CONNECTION_ID&limit=25&offset=0&template=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "template": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/list-questionnaire-results?${params}`, {
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
| `template` | string | yes | Questionnaire template entity name returned by List Questionnaire Templates. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated questionnaire result fields to return. |
| `expand` | string | no | OData expand expression for nested questionnaire results. |
| `filter` | string | no | OData filter expression. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Resco Cloud API returns.

## Native endpoint

Through the native Resco Cloud API, this operation is `GET https://{{credentials.organization}}.rescocrm.com/odata/questionnaires/v4/:template` (base URL `https://{{credentials.organization}}.app.resco.net/rest/v1/data`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-questionnaire-results.md) for the provider-specific parameters and requirements.

