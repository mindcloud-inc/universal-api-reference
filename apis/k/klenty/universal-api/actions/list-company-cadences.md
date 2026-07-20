# Klenty: List Company Cadences

Retrieves company cadences from Klenty.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-company-cadences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-company-cadences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-company-cadences?${params}`, {
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
      "createdDate": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "owner": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `owner` | string |  |

## Native endpoint

Through the native Klenty API, this operation is `GET /cadences` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-cadences.md) for the provider-specific parameters and requirements.

