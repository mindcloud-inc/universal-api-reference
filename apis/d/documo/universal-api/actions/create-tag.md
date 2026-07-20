# Documo: Create Tag

Creates a new tag in Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "color": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Tag name. |
| `color` | string | yes | Hex color with leading #. |
| `isPublic` | boolean | no | Whether the tag is visible to all account users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `color` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `POST /v1/tag` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

