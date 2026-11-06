# Microsoft Dynamics 365 Sales: Get Table Definition



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/get-table-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/get-table-definition?connectionId=$CONNECTION_ID&logicalName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logicalName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/get-table-definition?${params}`, {
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
| `logicalName` | string | yes | LogicalName returned by List Tables, such as account or new_project. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no |  |
| `expand` | string | no | OData relationship expression specifying related records to include. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 Sales API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `GET /EntityDefinitions(LogicalName=':logicalName')` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-definition.md) for the provider-specific parameters and requirements.

