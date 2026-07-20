# Hy.page: List Meeting Slots



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-meeting-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-meeting-slots?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-meeting-slots?${params}`, {
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
| `productId` | string | yes | Meeting product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productId": "string",
      "productTitle": "string",
      "slots": [
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
| `productId` | string |  |
| `productTitle` | string |  |
| `slots` | array<object> |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/meetings/slots` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meeting-slots.md) for the provider-specific parameters and requirements.

