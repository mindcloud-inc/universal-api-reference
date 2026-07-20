# CompanyCam: List Tags



```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-tags?${params}`, {
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
      "id": "string",
      "displayValue": "string",
      "value": "string",
      "tagType": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `displayValue` | string |  |
| `value` | string |  |
| `tagType` | string |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET tags` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

