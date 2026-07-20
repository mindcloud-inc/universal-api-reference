# Supernotes: Get All Templates

Retrieves all of your Supernotes templates.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-all-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-all-templates?${params}`, {
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
      "createdWhen": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "markup": "string",
      "modifiedWhen": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdWhen` | date |  |
| `id` | string |  |
| `markup` | string |  |
| `modifiedWhen` | date |  |
| `name` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /templates` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-templates.md) for the provider-specific parameters and requirements.

