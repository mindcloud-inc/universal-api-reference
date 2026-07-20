# Sendible: List Quick Reports



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-quick-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-quick-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-quick-reports?${params}`, {
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
      "id": 1,
      "report_header": "string",
      "report_title": "string",
      "report_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `report_header` | string |  |
| `report_title` | string |  |
| `report_type` | string |  |

## Native endpoint

Through the native Sendible API, this operation is `GET api/v2/quick_reports.json` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quick-reports.md) for the provider-specific parameters and requirements.

