# Lara Translate: List translation memories

Retrieves translation memories from Lara Translate.

```
GET https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/list-translation-memories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/list-translation-memories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/list-translation-memories?${params}`, {
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
| `collaboratorsCount` | number | Number of collaborators. |
| `createdAt` | date | Creation timestamp. |
| `externalId` | string | External source ID. |
| `id` | string | Translation memory ID. |
| `isPersonal` | boolean | Whether the memory is personal. |
| `name` | string | Translation memory name. |
| `ownerId` | string | Owner account ID. |
| `secret` | string | Memory secret. |
| `sharedAt` | date | Sharing timestamp. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-translation-memories.md) for the provider-specific parameters and requirements.

