# Microsoft Dynamics 365 Sales: Update Custom Record



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-custom-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-custom-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entitySetName": "new_projects",
  "recordId": "00000000-0000-0000-0000-000000000001",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-custom-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entitySetName": "new_projects",
    "recordId": "00000000-0000-0000-0000-000000000001",
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entitySetName` | string | yes | EntitySetName returned by List Tables. Use this exact API collection name, not the display label or a guessed plural. Example: `new_projects`. |
| `recordId` | string | yes | Example: `00000000-0000-0000-0000-000000000001`. |
| `fields` | object | yes | An object mapping the custom table's column logical names to their new values. Use List Table Columns to find writable columns. This schema varies by your environment. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated column logical names to return. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 Sales API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `PATCH /:entitySetName(:recordId)` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-record.md) for the provider-specific parameters and requirements.

