# Tomba: Retrieve API Usage

Retrieves API usage details from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/retrieve-api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/retrieve-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/retrieve-api-usage?${params}`, {
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
      "": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "search": 1,
          "sources": 1,
          "user_id": 1,
          "verifier": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].created_at` | date |  |
| `[].id` | number |  |
| `[].search` | number |  |
| `[].sources` | number |  |
| `[].user_id` | number |  |
| `[].verifier` | number |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /usage` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-api-usage.md) for the provider-specific parameters and requirements.

