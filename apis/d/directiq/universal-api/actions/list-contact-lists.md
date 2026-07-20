# DirectIQ: List Contact Lists

Retrieves all contact lists from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contact-lists?${params}`, {
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
      "bounceEstimate": 1,
      "clientId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "quality": 1,
      "totalActive": 1,
      "totalCount": 1,
      "totalDisabled": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceEstimate` | number |  |
| `clientId` | number |  |
| `createdDate` | date |  |
| `id` | number |  |
| `lastModified` | date |  |
| `name` | string |  |
| `quality` | number |  |
| `totalActive` | number |  |
| `totalCount` | number |  |
| `totalDisabled` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/lists/list` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

