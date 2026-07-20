# Caspio: List Views

Retrieves all available views from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-views?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-views?${params}`, {
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
      "Result": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | array<string> |  |

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/views` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-views.md) for the provider-specific parameters and requirements.

