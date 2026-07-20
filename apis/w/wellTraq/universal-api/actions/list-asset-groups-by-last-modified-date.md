# WellTraq: List Asset Groups By Last Modified Date

Retrieves asset groups from WellTraq by last modified date.

```
GET https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-asset-groups-by-last-modified-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WellTraq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-asset-groups-by-last-modified-date?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-asset-groups-by-last-modified-date?${params}`, {
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
      "description": "string",
      "id": "string",
      "lastModifiedDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `lastModifiedDate` | date |  |
| `name` | string |  |

## Native endpoint

Through the native WellTraq API, this operation is `GET /AssetGroups/ByLastModifiedDate` (base URL `https://welltraq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asset-groups-by-last-modified-date.md) for the provider-specific parameters and requirements.

