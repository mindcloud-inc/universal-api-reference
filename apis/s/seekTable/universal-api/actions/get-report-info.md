# SeekTable: Get Report Info

Retrieves a SeekTable report by report ID.

```
GET https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/get-report-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/get-report-info?connectionId=$CONNECTION_ID&reportId=edb1ee25d81c4acd96d2c9d0f819afde" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "edb1ee25d81c4acd96d2c9d0f819afde"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/get-report-info?${params}`, {
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
| `reportId` | string | yes | GUID of the report saved in your SeekTable account. Example: `edb1ee25d81c4acd96d2c9d0f819afde`. |

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

Through the native SeekTable API, this operation is `GET /api/report/:report_id` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-info.md) for the provider-specific parameters and requirements.

