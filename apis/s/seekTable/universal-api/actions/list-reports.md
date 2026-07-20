# SeekTable: List Reports

Retrieves saved reports from your SeekTable account.

```
GET https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/list-reports?${params}`, {
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
      "canEdit": true,
      "canShareToTeam": true,
      "config": "string",
      "createDate": "string",
      "cubeId": "string",
      "id": "string",
      "isPublic": true,
      "isSubscribed": true,
      "name": "Ava Chen",
      "reportType": "string",
      "shared": true,
      "updateDate": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canEdit` | boolean |  |
| `canShareToTeam` | boolean |  |
| `config` | string |  |
| `createDate` | string |  |
| `cubeId` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `isSubscribed` | boolean |  |
| `name` | string |  |
| `reportType` | string |  |
| `shared` | boolean |  |
| `updateDate` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SeekTable API, this operation is `GET /api/report` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

