# MRPeasy: List BOMs

Retrieves bills of materials from MRPeasy.

```
GET https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/list-boms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/list-boms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/list-boms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `GET /boms` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boms.md) for the provider-specific parameters and requirements.

