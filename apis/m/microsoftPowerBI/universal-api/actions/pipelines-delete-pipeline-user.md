# Microsoft Power BI: Delete Pipeline User



```
DELETE https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/pipelines-delete-pipeline-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/pipelines-delete-pipeline-user?connectionId=$CONNECTION_ID&pipelineId=string&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "string",
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/pipelines-delete-pipeline-user?${params}`, {
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
| `pipelineId` | string | yes | The deployment pipeline ID |
| `identifier` | string | yes | To delete user pipeline permissions, provide the user principal name (UPN) of the user. To delete a service principal or a security group's pipeline permissions, provide the Object ID of the service principal or security group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `DELETE pipelines/[:pipelineId]/users/[:identifier]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pipelines-delete-pipeline-user.md) for the provider-specific parameters and requirements.

