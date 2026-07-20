# Microsoft Power BI: Reports GenerateTokenInGroup



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/embed-token-reports-generatetoken-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/embed-token-reports-generatetoken-in-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "reportId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/embed-token-reports-generatetoken-in-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "reportId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID |
| `reportId` | string | yes | The report ID |
| `accessLevel` | object | no | The required access level for embed token generation |
| `allowSaveAs` | boolean | no | Whether an embedded report can be saved as a new report. The default value is false. Only applies when you generate an embed token for report embedding. |
| `datasetId` | string | no | The dataset ID used for report creation. Only applies when you generate an embed token for report creation. |
| `identities[]` | array<object> | no | A list of identities to use for row-level security rules |
| `lifetimeInMinutes` | number | no | The maximum lifetime of the token in minutes, starting from the time it was generated. Can be used to shorten the expiration time of a token, but not to extend it. The value must be a positive integer. Zero (0) is equivalent to null and will be ignored, resulting in the default expiration time. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/reports/[:reportId]/GenerateToken` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/embed-token-reports-generatetoken-in-group.md) for the provider-specific parameters and requirements.

