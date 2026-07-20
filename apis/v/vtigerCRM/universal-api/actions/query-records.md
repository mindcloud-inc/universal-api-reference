# Vtiger CRM: Query Records

Finds records in Vtiger CRM by query string.

```
GET https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/query-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/query-records?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/query-records?${params}`, {
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
| `query` | string | yes | Vtiger query string, for example select id, firstname, lastname from Contacts limit 0, 2; |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger record id when selected by the query. |
| `label` | string | Vtiger record label when returned by the query. |
| `url` | string | Vtiger record URL when returned by the query. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `GET /query` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-records.md) for the provider-specific parameters and requirements.

