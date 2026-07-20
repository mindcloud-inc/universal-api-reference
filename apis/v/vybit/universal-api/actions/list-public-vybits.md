# Vybit: List Public Vybits



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-public-vybits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-public-vybits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-public-vybits?${params}`, {
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
| `limit` | number | no | Maximum number of records to return |
| `offset` | number | no | Number of records to skip for pagination |
| `search` | string | no | Text search query |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "following": true,
      "imageUrl": "https://example.com",
      "key": "string",
      "linkUrl": "https://example.com",
      "name": "Ava Chen",
      "ownerName": "Ava Chen",
      "soundKey": "string",
      "soundType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `following` | boolean |  |
| `imageUrl` | string |  |
| `key` | string |  |
| `linkUrl` | string |  |
| `name` | string |  |
| `ownerName` | string |  |
| `soundKey` | string |  |
| `soundType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Vybit API, this operation is `GET /subscriptions/public` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-vybits.md) for the provider-specific parameters and requirements.

