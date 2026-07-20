# Attio: Delete List Entry

Deletes a list entry from Attio.

```
DELETE https://connect.mindcloud.co/v1/universal/attio/latest/actions/delete-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/attio/latest/actions/delete-list-entry?connectionId=$CONNECTION_ID&list=string&entry_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "string",
  "entry_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/delete-list-entry?${params}`, {
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
| `list` | string | yes | The UUID or slug identifying the list. |
| `entry_id` | string | yes | The UUID identifying the list entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | The raw response body. The saved successful response was an empty object. |

## Native endpoint

Through the native Attio API, this operation is `DELETE /v2/lists/:list/entries/:entry_id` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list-entry.md) for the provider-specific parameters and requirements.

