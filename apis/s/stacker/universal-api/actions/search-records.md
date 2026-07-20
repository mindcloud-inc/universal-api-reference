# Stacker: Search Records

Finds records in a Stacker object.

```
GET https://connect.mindcloud.co/v1/universal/stacker/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stacker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/search-records?connectionId=$CONNECTION_ID&accountId=string&objectSid=string&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "objectSid": "string",
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacker/latest/actions/search-records?${params}`, {
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
| `accountId` | string | yes | Stacker account ID sent as the X-Account-Id header. |
| `count` | number | no | Maximum number of records to return. |
| `filters[]` | array<object> | no | Array of filter conditions for the record search. |
| `includeFields[]` | array<string> | no | Field API names to include in the response. |
| `objectSid` | string | yes | Object SID from the Stacker endpoint path. |
| `orderBy` | string | no | Field API name to sort by. Prefix with '-' for descending order. |
| `search` | string | no | Text to search across the selected fields. |
| `searchFields[]` | array<string> | no | Field API names to search across. |
| `stackId` | string | yes | Stacker stack ID sent as the X-Stack-Id header. |
| `start` | number | no | Zero-based starting index for the returned records. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stacker API returns.

## Native endpoint

Through the native Stacker API, this operation is `POST /api/external/objects/:object_sid/search/` (base URL `https://api.go.stackerhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

