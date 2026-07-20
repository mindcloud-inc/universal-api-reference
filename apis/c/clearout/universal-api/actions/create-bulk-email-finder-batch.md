# Clearout: Create Bulk Email Finder Batch

Creates a bulk email finder batch in Clearout.

```
POST https://connect.mindcloud.co/v1/universal/clearout/latest/actions/create-bulk-email-finder-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/create-bulk-email-finder-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clearout/latest/actions/create-bulk-email-finder-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreDuplicateFile` | string | no | Whether to allow file with the same name and size that match with your recent upload Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listId` | string |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /email_finder/bulk` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-email-finder-batch.md) for the provider-specific parameters and requirements.

