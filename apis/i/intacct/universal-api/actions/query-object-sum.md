# Sage Intacct: Query Object Sum



```
GET https://connect.mindcloud.co/v1/universal/intacct/latest/actions/query-object-sum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/query-object-sum?connectionId=$CONNECTION_ID&limit=25&offset=0&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intacct/latest/actions/query-object-sum?${params}`, {
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
| `filter[].filterfield` | string | no |  |
| `object` | string | no |  |
| `options[].caseinsensitive` | boolean | no |  |
| `fields[]` | array<string> | yes |  |
| `filter[].filtertype` | list<string> | no |  |
| `options[].showprivate` | boolean | no | In a multi-entity company, set the `showprivate` element to `true` to query data in private entities. |
| `filter[]` | array<object> | no |  |
| `filter[].filtervalue` | string | no |  |
| `docparid` | string | no |  |
| `entityID` | string | no |  |
| `options[]` | array | no |  |
| `orderBy` | string | no |  |
| `sumField` | string | no | Return the sum of the fields. The fields in the select element are used to group the results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-object-sum.md) for the provider-specific parameters and requirements.

