# xMatters: Get subscription forms

Retrieves subscription forms from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscription-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscription-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscription-forms?${params}`, {
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
          "created": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "form": {
            "id": "string",
            "name": "Ava Chen"
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "notificationDelay": 1,
          "oneWay": true,
          "plan": {
            "id": "string",
            "name": "Ava Chen"
          },
          "scope": "string",
          "self": "string",
          "subscribeOthers": true
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
| `data[].created` | date |  |
| `data[].description` | string |  |
| `data[].form.id` | string |  |
| `data[].form.name` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].notificationDelay` | number |  |
| `data[].oneWay` | boolean |  |
| `data[].plan.id` | string |  |
| `data[].plan.name` | string |  |
| `data[].scope` | string |  |
| `data[].self` | string |  |
| `data[].subscribeOthers` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET subscription-forms` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-subscription-forms.md) for the provider-specific parameters and requirements.

