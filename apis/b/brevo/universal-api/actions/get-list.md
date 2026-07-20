# Brevo: Get List



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-list?${params}`, {
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
| `listId` | string | yes | Brevo list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "dynamicList": true,
      "endDate": "string",
      "folderId": 1,
      "id": 1,
      "name": "Ava Chen",
      "startDate": "string",
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
| `createdAt` | string |  |
| `dynamicList` | boolean |  |
| `endDate` | string |  |
| `folderId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `startDate` | string |  |
| `totalBlacklisted` | number |  |
| `totalSubscribers` | number |  |
| `uniqueSubscribers` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/lists/:listId` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

