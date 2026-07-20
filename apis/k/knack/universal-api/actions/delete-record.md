# Knack: Delete Record



```
DELETE https://connect.mindcloud.co/v1/universal/knack/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Knack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/knack/latest/actions/delete-record?connectionId=$CONNECTION_ID&objectKey=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectKey": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knack/latest/actions/delete-record?${params}`, {
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
| `recordId` | string | yes | Knack record ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "delete": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delete` | boolean | Whether the Knack record was deleted. |

## Native endpoint

Through the native Knack API, this operation is `DELETE /objects/:object_key/records/:record_id` (base URL `https://api.knack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

