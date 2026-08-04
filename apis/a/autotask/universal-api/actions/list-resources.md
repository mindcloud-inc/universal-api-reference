# Autotask: List Resources



```
GET https://connect.mindcloud.co/v1/universal/autotask/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/list-resources?connectionId=$CONNECTION_ID&filters%5B%5D=%5Bobject%20Object%5D&filters%5B%5D.field=lastName&filters%5B%5D.operator=beginsWith&filters%5B%5D.valueType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters[]": "[object Object]",
  "filters[].field": "lastName",
  "filters[].operator": "beginsWith",
  "filters[].valueType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autotask/latest/actions/list-resources?${params}`, {
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
| `filters[]` | array<object> | yes | Build one or more Autotask filter conditions. Conditions are combined with AND. |
| `filters[].field` | string | yes | Autotask entity field name to filter, such as id or companyName. Example: `lastName`. |
| `filters[].operator` | list<string> | yes | Comparison operator applied between the field and value. One of: `beginsWith`, `contains`, `endsWith`, `eq`, `exist`, `gt`, `gte`, `in`, `lt`, `lte`, `notExist`, `notIn`, `noteq`. |
| `filters[].valueType` | list<string> | yes | How to encode the filter value. Dates and timestamps should use String with the Autotask-supported format. One of: `boolean`, `number`, `string`. Default: `string`. |
| `filters[].value` | string | no | Value for scalar operators. Leave empty for Exists, Does Not Exist, In, and Not In. Example: `Smith`. |
| `filters[].list[]` | array<string> | no | Values for In or Not In operators. |
| `filters[].udf` | boolean | no | Enable when Field names an Autotask user-defined field. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autotask API returns.

## Native endpoint

Through the native Autotask API, this operation is `GET /Resources/query` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

