# xMatters: Get forms

Retrieves forms from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-forms?${params}`, {
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
      "count": 1,
      "data": [
        {
          "apiEnabled": true,
          "description": "string",
          "formId": "string",
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "mobileEnabled": true,
          "name": "Ava Chen",
          "plan": {
            "id": "string",
            "name": "Ava Chen"
          },
          "self": "string",
          "senderOverrides": {
            "callerId": "string",
            "displayName": "Ava Chen"
          },
          "uiEnabled": true
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].apiEnabled` | boolean |  |
| `data[].description` | string |  |
| `data[].formId` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].mobileEnabled` | boolean |  |
| `data[].name` | string |  |
| `data[].plan.id` | string |  |
| `data[].plan.name` | string |  |
| `data[].self` | string |  |
| `data[].senderOverrides.callerId` | string |  |
| `data[].senderOverrides.displayName` | string |  |
| `data[].uiEnabled` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET forms` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-forms.md) for the provider-specific parameters and requirements.

