# Brevo: Get Contact Folder



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact-folder?connectionId=$CONNECTION_ID&folderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact-folder?${params}`, {
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
| `folderId` | number | yes | The contact folder identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "totalBlacklisted": 1,
      "totalSubscribers": 1,
      "uniqueSubscribers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The folder id. |
| `name` | string | The folder name. |
| `totalBlacklisted` | number | The number of blacklisted contacts. |
| `totalSubscribers` | number | The number of subscribers. |
| `uniqueSubscribers` | number | The number of unique subscribers. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/folders/:folderId` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-folder.md) for the provider-specific parameters and requirements.

