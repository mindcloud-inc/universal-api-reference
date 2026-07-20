# ActivityInfo: List Reports

Retrieves available reports from your ActivityInfo account.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-reports?${params}`, {
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
      "icon": "string",
      "id": "string",
      "label": "string",
      "lastUpdateTime": 1,
      "owned": true,
      "published": true,
      "shared": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `icon` | string | Report display icon. |
| `id` | string | Report ID. |
| `label` | string | Report title. |
| `lastUpdateTime` | number | Last report definition update time. |
| `owned` | boolean | Whether the authenticated user owns the report. |
| `published` | boolean | Whether the report has been published. |
| `shared` | boolean | Whether the report is shared. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/reports` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

