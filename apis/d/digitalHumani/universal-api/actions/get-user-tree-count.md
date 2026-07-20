# Digital Humani: Get User Tree Count

Retrieves a user's tree count from Digital Humani.

```
GET https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-user-tree-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-user-tree-count?connectionId=$CONNECTION_ID&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-user-tree-count?${params}`, {
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
| `user` | string | yes | The user whose tree count you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "enterpriseId": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `enterpriseId` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Digital Humani API, this operation is `GET /tree` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-tree-count.md) for the provider-specific parameters and requirements.

