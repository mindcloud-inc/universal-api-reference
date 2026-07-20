# noCRM.io: List Pipelines

Retrieves pipelines from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-pipelines?${params}`, {
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
      "createdAt": "string",
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /pipelines` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

