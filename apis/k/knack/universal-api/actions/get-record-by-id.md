# Knack: Get Record By ID



```
GET https://connect.mindcloud.co/v1/universal/knack/latest/actions/get-record-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Knack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knack/latest/actions/get-record-by-id?connectionId=$CONNECTION_ID&objectKey=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectKey": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knack/latest/actions/get-record-by-id?${params}`, {
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
| `objectKey` | string | yes | Knack object key from the Builder URL, such as object_3. |
| `recordId` | string | yes | Knack record ID to retrieve, such as 69b4423b3c1f982951ba5309. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Knack API returns.

## Native endpoint

Through the native Knack API, this operation is `GET /objects/:object_key/records/:record_id` (base URL `https://api.knack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-by-id.md) for the provider-specific parameters and requirements.

