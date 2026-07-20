# Maildrip: Get UTM attribution breakdown for an opt-in page's signups



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-utm-attribution-breakdown-for-an-opt-in-page-s-signups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-utm-attribution-breakdown-for-an-opt-in-page-s-signups?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-utm-attribution-breakdown-for-an-opt-in-page-s-signups?${params}`, {
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
| `pageId` | string | yes | ID of the opt-in page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by_campaign": [
        {}
      ],
      "by_medium": [
        {}
      ],
      "by_source": [
        {}
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
| `by_campaign` | array<object> |  |
| `by_medium` | array<object> |  |
| `by_source` | array<object> |  |
| `total` | number | Total signup events recorded for this opt-in page |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/opt-in-pages/{pageId}/stats/utm` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-utm-attribution-breakdown-for-an-opt-in-page-s-signups.md) for the provider-specific parameters and requirements.

