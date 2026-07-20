# Nova: Get Live Lists



```
GET https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-live-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-live-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-live-lists?${params}`, {
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
      "choices": [
        {
          "label": "string",
          "sample": "string",
          "value": "string"
        }
      ],
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> | Available live list choices for the authenticated company. |
| `choices[].label` | string | Human-readable live list label. |
| `choices[].sample` | string | Sample list identifier value. |
| `choices[].value` | string | Actual list identifier value. |
| `key` | string | Returned selector key for the list identifier field. |

## Native endpoint

Through the native Nova API, this operation is `GET /admin/company/live-lists` (base URL `https://app.n0va.com/v1/la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-lists.md) for the provider-specific parameters and requirements.

