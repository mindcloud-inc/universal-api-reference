# Baremetrics: List Fields

Retrieves segment fields from Baremetrics.

```
GET https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `GET /v1/segments/fields` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

