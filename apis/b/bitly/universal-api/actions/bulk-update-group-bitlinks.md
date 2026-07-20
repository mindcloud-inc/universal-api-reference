# Bitly: Bulk Update Group Bitlinks

Updates tags or archives multiple group bitlinks in Bitly.

```
PUT https://connect.mindcloud.co/v1/universal/bitly/latest/actions/bulk-update-group-bitlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/bulk-update-group-bitlinks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "groupGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/bulk-update-group-bitlinks', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "groupGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | The bulk update operation to apply. |
| `addTags[]` | array<string> | no | Tags to add to the selected links. |
| `archive` | boolean | no | Whether to archive the selected links. |
| `groupGuid` | string | yes | The Bitly group GUID. |
| `links[]` | array<string> | no | The bitlink IDs to update in bulk. |
| `removeTags[]` | array<string> | no | Tags to remove from the selected links. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links[]` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `PATCH /groups/:group_guid/bitlinks` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-group-bitlinks.md) for the provider-specific parameters and requirements.

