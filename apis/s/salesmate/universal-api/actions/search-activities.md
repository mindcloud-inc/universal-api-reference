# Salesmate: Search Activities



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-activities?${params}`, {
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
| `filterQuery` | object | no | Salesmate search filter object. Default: `{"group":{"rules":[{"data":"Jan 01, 1970 05:30 AM","field":{"type":"DateTime","fieldName":"activity.createdAt","displayName":"Created At"},"condition":"IS_AFTER","eventType":"DateTime","moduleName":"Task"}],"operator":"AND"}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dueDate": 1,
      "id": 1,
      "isCompleted": 1,
      "owner": 1,
      "title": "string",
      "type": "string",
      "typeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dueDate` | number |  |
| `id` | number |  |
| `isCompleted` | number |  |
| `owner` | number |  |
| `title` | string |  |
| `type` | string |  |
| `typeId` | string |  |

## Native endpoint

Through the native Salesmate API, this operation is `POST /activity/v4/search` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-activities.md) for the provider-specific parameters and requirements.

