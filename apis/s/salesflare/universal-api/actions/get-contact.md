# Salesflare: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | The Salesflare contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "archived": true,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "email": "ava@example.com",
      "id": 1,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `archived` | boolean |  |
| `creationDate` | date |  |
| `domain` | string |  |
| `email` | string |  |
| `id` | number |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `owner` | object |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET contacts` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

