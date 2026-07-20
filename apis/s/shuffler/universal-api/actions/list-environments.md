# Shuffler: List Environments

Retrieves environments from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-environments?${params}`, {
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
      "default": true,
      "id": "string",
      "Name": "Ava Chen",
      "orgId": "string",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `id` | string |  |
| `Name` | string |  |
| `orgId` | string |  |
| `Type` | string |  |

## Native endpoint

Through the native Shuffler API, this operation is `GET /getenvironments` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

