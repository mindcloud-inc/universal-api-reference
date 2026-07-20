# Teletype App: Get Project Details

Retrieves project details from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-details?${params}`, {
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
      "createdAt": {},
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | object |  |
| `domain` | string |  |
| `id` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /project/details` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-details.md) for the provider-specific parameters and requirements.

