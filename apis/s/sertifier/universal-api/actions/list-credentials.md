# Sertifier: List Credentials

Finds credentials in Sertifier by search filters.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-credentials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-credentials?${params}`, {
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
| `startIndex` | number | no | Default: `0`. |
| `length` | number | no | Default: `10`. |
| `status` | number | no | Example: `1`. |
| `searchTerm` | string | no | Example: `credential name or email`. |
| `campaignIds[]` | array<string> | no | Accepts multiple values as an array. Example: `campaign-id`. |
| `recipientIds[]` | array<string> | no | Accepts multiple values as an array. Example: `recipient-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeImageLink": {},
      "campaignId": "string",
      "campaignTitle": "string",
      "certificateImageLink": {},
      "certificateNO": "string",
      "createDate": "string",
      "email": {},
      "emailTracking": 1,
      "expireDate": {},
      "id": "string",
      "isPublic": true,
      "issueDate": "string",
      "name": "Ava Chen",
      "recipientId": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeImageLink` | object |  |
| `campaignId` | string |  |
| `campaignTitle` | string |  |
| `certificateImageLink` | object |  |
| `certificateNO` | string |  |
| `createDate` | string |  |
| `email` | object |  |
| `emailTracking` | number |  |
| `expireDate` | object |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `issueDate` | string |  |
| `name` | string |  |
| `recipientId` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /credential/search` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credentials.md) for the provider-specific parameters and requirements.

