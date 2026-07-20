# Microsoft Power BI: Post Dataset User



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-post-dataset-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-post-dataset-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "datasetUserAccessRight": "string",
  "identifier": "string",
  "principalType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-post-dataset-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "datasetUserAccessRight": "string",
    "identifier": "string",
    "principalType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | The dataset ID |
| `datasetUserAccessRight` | list | yes | Required. The access right to grant to the user for the dataset. |
| `identifier` | string | yes | For principal type User, provide the *UPN*. Otherwise provide the object ID of the principal. |
| `principalType` | list | yes | The principal type |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST datasets/[:datasetId]/users` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datasets-post-dataset-user.md) for the provider-specific parameters and requirements.

