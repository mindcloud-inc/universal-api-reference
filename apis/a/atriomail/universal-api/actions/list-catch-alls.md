# Atriomail: List Catch-Alls



```
GET https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-catch-alls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-catch-alls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-catch-alls?${params}`, {
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
      "active": true,
      "address": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "domain": "string",
      "domainId": 1,
      "goto": "string",
      "gotoArray": [
        "string"
      ],
      "id": 1,
      "isCatchAll": true,
      "mailcowId": 1,
      "privateComment": "string",
      "syncedAt": "2026-05-07T12:00:00.000Z",
      "syncStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | string |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `domain` | string |  |
| `domainId` | number |  |
| `goto` | string |  |
| `gotoArray` | array<string> |  |
| `id` | number |  |
| `isCatchAll` | boolean |  |
| `mailcowId` | number |  |
| `privateComment` | string |  |
| `syncedAt` | date |  |
| `syncStatus` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Atriomail API, this operation is `GET /catch-all` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-catch-alls.md) for the provider-specific parameters and requirements.

