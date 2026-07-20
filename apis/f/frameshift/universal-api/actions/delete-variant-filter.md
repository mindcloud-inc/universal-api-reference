# Frameshift: Delete Variant Filter

Deletes an existing variant filter from Frameshift.

```
DELETE https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/delete-variant-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/delete-variant-filter?connectionId=$CONNECTION_ID&projectId=string&variantFilterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "variantFilterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/delete-variant-filter?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |
| `variantFilterId` | string | yes | Resource identifier for the variant filter to access |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frameshift API returns.

## Native endpoint

Through the native Frameshift API, this operation is `DELETE /v1/projects/:project_id/variants/filters/:variant_filter_id` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-variant-filter.md) for the provider-specific parameters and requirements.

