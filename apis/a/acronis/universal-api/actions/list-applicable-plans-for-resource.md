# Acronis: List Applicable Plans For Resource

Retrieves protection plans applicable to a resource in Acronis.

```
GET https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-applicable-plans-for-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acronis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-applicable-plans-for-resource?connectionId=$CONNECTION_ID&applicableToContextId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicableToContextId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-applicable-plans-for-resource?${params}`, {
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
| `applicableToContextId` | string | yes | Resource ID used to find applicable protection plans. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeAppliedContext` | boolean | no | When true, include applied context details in the response. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acronis API returns.

## Native endpoint

Through the native Acronis API, this operation is `GET /api/policy_management/v4/policies` (base URL `{{credentials.dataCenterUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applicable-plans-for-resource.md) for the provider-specific parameters and requirements.

