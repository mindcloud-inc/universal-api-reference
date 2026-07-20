# Maildrip: Preview segment membership without saving



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/preview-segment-membership-without-saving
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/preview-segment-membership-without-saving?connectionId=$CONNECTION_ID&filters%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/preview-segment-membership-without-saving?${params}`, {
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
| `filters[]` | array<object> | yes | Array of filter objects Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/segments/preview` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-segment-membership-without-saving.md) for the provider-specific parameters and requirements.

