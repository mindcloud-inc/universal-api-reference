# Print.one Postcards: Create Template Preview

Creates a new template preview in Print.one Postcards.

```
POST https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-template-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-template-preview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "version": 1,
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-template-preview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "version": 1,
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Template ID. |
| `version` | number | yes | Template version. |
| `firstName` | string | yes | Merge variable for the template preview. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asPdf` | boolean | no | Return the preview as PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detailsUrl": "https://example.com",
      "orderingKey": 1,
      "url": "https://example.com",
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detailsUrl` | string |  |
| `orderingKey` | number |  |
| `url` | string |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `POST /v2/templates/preview/[:id]/[:version]` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-preview.md) for the provider-specific parameters and requirements.

