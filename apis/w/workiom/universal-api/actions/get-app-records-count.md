# Workiom: Get App Records Count

Retrieves an app's record count from Workiom.

```
GET https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-app-records-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-app-records-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-app-records-count?${params}`, {
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
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native Workiom API, this operation is `GET /api/services/app/Data/GetAppRecordsCount` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-records-count.md) for the provider-specific parameters and requirements.

