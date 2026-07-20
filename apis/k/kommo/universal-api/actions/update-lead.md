# Kommo: Update Lead



```
PUT https://connect.mindcloud.co/v1/universal/kommo/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kommo/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommo/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Lead ID. |
| `name` | string | no | Lead name. |
| `price` | number | no | Lead price. |
| `statusId` | number | no | Lead status ID. |
| `pipelineId` | number | no | Lead pipeline ID. |
| `lossReasonId` | number | no | Loss reason ID. |
| `responsibleUserId` | number | no | Responsible user ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFieldsValues[]` | array<object> | no | Custom field values payload. |
| `embedded` | object | no | Embedded payload. |
| `requestId` | string | no | Request identifier. |
| `tagsToAdd[]` | array<object> | no | Tags to add payload. |
| `tagsToDelete[]` | array<object> | no | Tags to delete payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp when returned by Kommo. |
| `id` | string | Unique identifier returned by Kommo. |
| `links.self.href` | string | Kommo API resource URL when returned in links. |
| `name` | string | Display name or title when returned by Kommo. |
| `updatedAt` | number | Last update timestamp when returned by Kommo. |

## Native endpoint

Through the native Kommo API, this operation is `PATCH /leads/:id` (base URL `https://{{credentials.authorizeRequest.referer}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

