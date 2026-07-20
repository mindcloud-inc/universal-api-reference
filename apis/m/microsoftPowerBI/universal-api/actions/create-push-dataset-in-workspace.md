# Microsoft Power BI: Create Push Dataset in Workspace



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/create-push-dataset-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/create-push-dataset-in-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "name": "Ava Chen",
  "tables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/create-push-dataset-in-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "name": "Ava Chen",
    "tables[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The Power BI workspace ID. |
| `name` | string | yes | The push dataset name. |
| `tables[]` | array<object> | yes | Array of table definitions for the push dataset. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `defaultRetentionPolicy` | list | no | Optional retention policy for the push dataset. Default: `basicFIFO`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultRetentionPolicy": "string",
      "id": "string",
      "name": "Ava Chen",
      "upstreamDatasets": [
        {}
      ],
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultRetentionPolicy` | string | Dataset retention policy. |
| `id` | string | Power BI dataset ID. |
| `name` | string | Dataset name. |
| `upstreamDatasets` | array<object> | Upstream dataset references when returned by Power BI. |
| `users` | array<object> | Dataset user access entries when returned by Power BI. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/datasets` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-push-dataset-in-workspace.md) for the provider-specific parameters and requirements.

