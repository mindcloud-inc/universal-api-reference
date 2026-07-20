# Klenty: List User Cadences

Retrieves user cadences from Klenty.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-user-cadences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-user-cadences?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-user-cadences?${params}`, {
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
| `username` | string | yes | Team member email address whose cadences should be listed. |

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

Through the native Klenty API, this operation is `GET /cadences` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-cadences.md) for the provider-specific parameters and requirements.

