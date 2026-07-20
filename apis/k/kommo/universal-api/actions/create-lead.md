# Kommo: Create Lead



```
POST https://connect.mindcloud.co/v1/universal/kommo/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kommo/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommo/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[].name` | string | no | Lead name |
| `[].price` | number | no | Lead sale Example: `9000`. |
| `[].statusId` | number | no | Stage ID the lead is added to. The first stage of the main pipeline by default. |
| `[].pipelineId` | number | no | Pipeline ID the lead is added to. |
| `[].responsibleUserId` | number | no | Lead responsible user ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[].customFieldsValues[]` | array<object> | no | An array of the current lead custom fields’ values. |
| `[].embedded` | object | no | Embedded entities of the lead. |
| `[].tagsToAdd[]` | array<object> | no | Tags attached to the lead. |

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

Through the native Kommo API, this operation is `POST /leads` (base URL `https://{{credentials.authorizeRequest.referer}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

