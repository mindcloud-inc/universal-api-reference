# Lara Translate: Rename translation memory

Updates an existing translation memory in Lara Translate.

```
PUT https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/rename-translation-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/rename-translation-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "mem_123",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/rename-translation-memory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "mem_123",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the translation memory to rename. Example: `mem_123`. |
| `name` | string | yes | New name for the translation memory. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collaboratorsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "isPersonal": true,
      "name": "Ava Chen",
      "ownerId": "string",
      "secret": "string",
      "sharedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collaboratorsCount` | number |  |
| `createdAt` | date |  |
| `externalId` | string |  |
| `id` | string |  |
| `isPersonal` | boolean |  |
| `name` | string |  |
| `ownerId` | string |  |
| `secret` | string |  |
| `sharedAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-translation-memory.md) for the provider-specific parameters and requirements.

