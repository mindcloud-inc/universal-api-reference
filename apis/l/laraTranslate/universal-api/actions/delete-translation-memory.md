# Lara Translate: Delete translation memory

Deletes an existing translation memory from Lara Translate.

```
DELETE https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/delete-translation-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/delete-translation-memory?connectionId=$CONNECTION_ID&id=mem_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "mem_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/delete-translation-memory?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the translation memory to delete. Example: `mem_123`. |

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

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-translation-memory.md) for the provider-specific parameters and requirements.

