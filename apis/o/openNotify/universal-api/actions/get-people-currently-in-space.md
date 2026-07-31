# Open Notify: Get People Currently in Space



```
GET https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-people-currently-in-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Notify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-people-currently-in-space?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-people-currently-in-space?${params}`, {
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
      "message": "string",
      "number": 1,
      "people": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider operation status. |
| `number` | number | Current number of people in space. |
| `people` | array<object> | People currently in space, each with name and craft. |

## Native endpoint

Through the native Open Notify API, this operation is `GET /astros.json` (base URL `http://api.open-notify.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-people-currently-in-space.md) for the provider-specific parameters and requirements.

