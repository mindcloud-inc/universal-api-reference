# MailBluster: List Fields

Retrieves all custom fields from MailBluster.

```
GET https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-fields?${params}`, {
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
      "fields": [
        {
          "createdAt": "string",
          "fieldLabel": "string",
          "fieldMergeTag": "string",
          "id": 1,
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Fields configured in the connected MailBluster brand. |
| `fields[].createdAt` | string | Creation timestamp. |
| `fields[].fieldLabel` | string | Field label. |
| `fields[].fieldMergeTag` | string | Field merge tag. |
| `fields[].id` | number | Unique field ID. |
| `fields[].updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `GET /fields` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

