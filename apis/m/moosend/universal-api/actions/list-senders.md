# Moosend: List Senders

Retrieves senders from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-senders?${params}`, {
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dkimPublic": "string",
      "dkimVerified": true,
      "dmarcVerified": true,
      "email": "ava@example.com",
      "id": "string",
      "isEnabled": true,
      "isVerified": true,
      "name": "Ava Chen",
      "spfVerified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `dkimPublic` | string |  |
| `dkimVerified` | boolean |  |
| `dmarcVerified` | boolean |  |
| `email` | string |  |
| `id` | string |  |
| `isEnabled` | boolean |  |
| `isVerified` | boolean |  |
| `name` | string |  |
| `spfVerified` | boolean |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /senders/find_all.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-senders.md) for the provider-specific parameters and requirements.

