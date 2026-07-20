# Zoho Recruit: Remove Tags

Removes tags from a Zoho Recruit record.

```
PUT https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/remove-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/remove-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "tagNames": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/remove-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "recordId": "string",
    "tagNames": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | string | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | string | yes | The unique ID of the Zoho Recruit record. |
| `tagNames` | string | yes | Tag names to remove from the record. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `details` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `POST /:moduleApiName/:recordId/actions/remove_tags` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tags.md) for the provider-specific parameters and requirements.

