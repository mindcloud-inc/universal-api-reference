# Microsoft Dynamics 365 Sales: List Leads



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/list-leads?${params}`, {
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
| `filter` | string | no | OData expression selecting matching records. Example: `createdon ge 2026-01-01T00:00:00Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated column logical names to return. Accepts multiple values in one string, delimited by `,`. |
| `expand` | string | no | OData relationship expression specifying related records to include. |
| `count` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 Sales API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `GET /leads` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

