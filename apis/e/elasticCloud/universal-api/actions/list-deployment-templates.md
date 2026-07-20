# Elastic Cloud: List Deployment Templates

Retrieves deployment templates from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployment-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployment-templates?connectionId=$CONNECTION_ID&region=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "region": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployment-templates?${params}`, {
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
| `region` | string | yes | Region of the deployment templates. |
| `metadata` | string | no | Optional metadata filter in key:value form. |
| `showInstanceConfigurations` | boolean | no | Return details for each instance configuration referenced by the template. |
| `showMaxZones` | boolean | no | Populate max_zones in instance configurations when instance configurations are shown. |
| `stackVersion` | string | no | Adapt returned templates to the given stack version. |
| `hideDeprecated` | boolean | no | Exclude templates flagged as deprecated. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Elastic Cloud API returns.

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/templates` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployment-templates.md) for the provider-specific parameters and requirements.

