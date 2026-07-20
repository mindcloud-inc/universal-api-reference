# Blueink: List Envelope Templates

Retrieves available envelope templates from Blueink.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-envelope-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-envelope-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-envelope-templates?${params}`, {
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
      "allowDirectSigning": true,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "documents": [
        {
          "key": "string",
          "name": "Ava Chen",
          "order": 1
        }
      ],
      "id": "string",
      "isPortal": true,
      "isShared": true,
      "name": "Ava Chen",
      "signers": [
        {
          "authId": true,
          "authSelfie": true,
          "authSms": true,
          "key": "string",
          "label": "string",
          "order": 1
        }
      ],
      "smartLinkUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowDirectSigning` | boolean |  |
| `created` | date |  |
| `description` | string |  |
| `documents[].key` | string |  |
| `documents[].name` | string |  |
| `documents[].order` | number |  |
| `id` | string |  |
| `isPortal` | boolean |  |
| `isShared` | boolean |  |
| `name` | string |  |
| `signers[].authId` | boolean |  |
| `signers[].authSelfie` | boolean |  |
| `signers[].authSms` | boolean |  |
| `signers[].key` | string |  |
| `signers[].label` | string |  |
| `signers[].order` | number |  |
| `smartLinkUrl` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /envelope-templates/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-envelope-templates.md) for the provider-specific parameters and requirements.

