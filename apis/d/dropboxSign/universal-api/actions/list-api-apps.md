# Dropbox Sign: List API Apps

Retrieves API apps from Dropbox Sign.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/list-api-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/list-api-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/list-api-apps?${params}`, {
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
      "callbackUrl": {},
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "domains": [
        "string"
      ],
      "isApproved": true,
      "name": "Ava Chen",
      "oauth": {},
      "options": {
        "canInsertEverywhere": true
      },
      "ownerAccount": {
        "accountId": "string",
        "emailAddress": "ava@example.com"
      },
      "whiteLabelingOptions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | object |  |
| `clientId` | string |  |
| `createdAt` | date |  |
| `domain` | string |  |
| `domains[]` | string |  |
| `isApproved` | boolean |  |
| `name` | string |  |
| `oauth` | object |  |
| `options.canInsertEverywhere` | boolean |  |
| `ownerAccount.accountId` | string |  |
| `ownerAccount.emailAddress` | string |  |
| `whiteLabelingOptions` | object |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /api_app/list` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-apps.md) for the provider-specific parameters and requirements.

