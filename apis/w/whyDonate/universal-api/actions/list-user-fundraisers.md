# WhyDonate: List User Fundraisers



```
GET https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/list-user-fundraisers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhyDonate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/list-user-fundraisers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/list-user-fundraisers?${params}`, {
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
      "data": {
        "count": "string",
        "results": [
          {}
        ]
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.count` | string |  |
| `data.results` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native WhyDonate API, this operation is `GET /fundraiser/wordpress/all` (base URL `https://fundraiser.whydonate.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-fundraisers.md) for the provider-specific parameters and requirements.

