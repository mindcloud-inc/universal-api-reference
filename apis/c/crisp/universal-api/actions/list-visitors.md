# Crisp: List Visitors

Retrieves visitors from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-visitors?connectionId=$CONNECTION_ID&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-visitors?${params}`, {
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
| `websiteId` | string | yes | The website identifier. |
| `pageNumber` | number | no | Page number for visitors paging. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "capabilities": [
        "string"
      ],
      "email": "ava@example.com",
      "geolocation": {},
      "inboxId": "string",
      "initiated": true,
      "lastPage": {},
      "locales": [
        "string"
      ],
      "nickname": "Ava Chen",
      "sessionId": "string",
      "timezone": 1,
      "useragent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatar` | string |  |
| `capabilities` | array<string> |  |
| `email` | string |  |
| `geolocation` | object |  |
| `inboxId` | string |  |
| `initiated` | boolean |  |
| `lastPage` | object |  |
| `locales` | array<string> |  |
| `nickname` | string |  |
| `sessionId` | string |  |
| `timezone` | number |  |
| `useragent` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/visitors/list/:page_number` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-visitors.md) for the provider-specific parameters and requirements.

