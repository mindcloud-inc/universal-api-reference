# Sign: Get dossier

Retrieves a dossier from CM.com Sign by ID.

```
GET https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-dossier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-dossier?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-dossier?${params}`, {
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
      "completed": true,
      "files": [
        {}
      ],
      "id": "string",
      "invitees": [
        {}
      ],
      "locale": "string",
      "name": "Ava Chen",
      "owners": [
        {}
      ],
      "reminderIn": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean |  |
| `files` | array<object> |  |
| `id` | string |  |
| `invitees` | array<object> |  |
| `locale` | string |  |
| `name` | string |  |
| `owners` | array<object> |  |
| `reminderIn` | number |  |
| `state` | string |  |

## Native endpoint

Through the native Sign API, this operation is `GET /dossiers/{dossierId}` (base URL `https://api.cm.com/sign-sandbox/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dossier.md) for the provider-specific parameters and requirements.

