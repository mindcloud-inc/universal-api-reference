# Microsoft Power BI: Get Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-workspace?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-workspace?${params}`, {
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
| `groupId` | string | yes | The workspace ID. |

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

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

