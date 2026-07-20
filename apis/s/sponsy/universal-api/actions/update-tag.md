# Sponsy: Update Tag

Updates a tag in Sponsy.

```
PUT https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": "string",
  "text": "string",
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": "string",
    "text": "string",
    "color": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | list<string> | yes | Tag ID from List Tags. |
| `text` | string | yes | Tag text. |
| `color` | string | yes | Tag hexadecimal color. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Tag hexadecimal color. |
| `createdAt` | date | Tag creation timestamp. |
| `id` | string | Sponsy tag ID. |
| `text` | string | Tag text. |
| `updatedAt` | date | Tag update timestamp. |

## Native endpoint

Through the native Sponsy API, this operation is `PATCH /v1/tags/:tagId` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

