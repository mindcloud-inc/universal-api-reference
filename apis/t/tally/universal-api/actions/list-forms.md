# Tally: List Forms



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-forms?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceIds` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "hasDraftBlocks": true,
      "id": "string",
      "index": 1,
      "isClosed": true,
      "isNameModifiedByUser": true,
      "name": "Ava Chen",
      "numberOfSubmissions": 1,
      "organizationId": "string",
      "status": "string",
      "updatedAt": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `hasDraftBlocks` | boolean |  |
| `id` | string |  |
| `index` | number |  |
| `isClosed` | boolean |  |
| `isNameModifiedByUser` | boolean |  |
| `name` | string |  |
| `numberOfSubmissions` | number |  |
| `organizationId` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET forms` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

