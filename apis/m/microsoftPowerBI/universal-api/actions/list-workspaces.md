# Microsoft Power BI: List Workspaces



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspaces?${params}`, {
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
| `filter` | string | no | OData filter expression for narrowing returned workspaces. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacityId": "string",
      "dataflowStorageId": "string",
      "defaultDatasetStorageFormat": "string",
      "id": "string",
      "isOnDedicatedCapacity": true,
      "isReadOnly": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacityId` | string | The capacity ID. |
| `dataflowStorageId` | string | The Power BI dataflow storage account ID. |
| `defaultDatasetStorageFormat` | string | The default dataset storage format. |
| `id` | string | The workspace ID. |
| `isOnDedicatedCapacity` | boolean | Whether the workspace is assigned to dedicated capacity. |
| `isReadOnly` | boolean | Whether the workspace is read-only. |
| `name` | string | The workspace name. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

