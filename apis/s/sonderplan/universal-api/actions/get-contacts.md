# Sonderplan: Get Contacts



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-contacts?${params}`, {
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
      "client": true,
      "created": 1,
      "email1": "ava@example.com",
      "id": 1,
      "linkedOrganizationId": 1,
      "linkedResourceId": 1,
      "name": "Ava Chen",
      "type": "string",
      "uuid": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | boolean |  |
| `created` | number |  |
| `email1` | string |  |
| `id` | number |  |
| `linkedOrganizationId` | number |  |
| `linkedResourceId` | number |  |
| `name` | string |  |
| `type` | string |  |
| `uuid` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /contact` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contacts.md) for the provider-specific parameters and requirements.

