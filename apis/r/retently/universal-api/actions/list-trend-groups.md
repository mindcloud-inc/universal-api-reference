# Retently: List Trend Groups

Retrieves a list of trend groups from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-trend-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-trend-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-trend-groups?${params}`, {
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
      "_id": "string",
      "createdDate": "string",
      "groupName": "Ava Chen",
      "isDefault": true,
      "metric": "string",
      "trendsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdDate` | string |  |
| `groupName` | string |  |
| `isDefault` | boolean |  |
| `metric` | string |  |
| `trendsCount` | number |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/trends` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trend-groups.md) for the provider-specific parameters and requirements.

