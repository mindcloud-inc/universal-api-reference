# Aspire: List Attachment Types



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-attachment-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-attachment-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-attachment-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "aspireSystemId": 1,
      "attachmentTypeID": 1,
      "attachmentTypeName": "Ava Chen",
      "canDelete": true,
      "required": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `aspireSystemId` | number |  |
| `attachmentTypeID` | number |  |
| `attachmentTypeName` | string |  |
| `canDelete` | boolean |  |
| `required` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `GET AttachmentTypes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-attachment-types.md) for the provider-specific parameters and requirements.

