# Middesk: Get TIN Match Availability

Retrieves TIN match availability from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-tin-match-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-tin-match-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-tin-match-availability?${params}`, {
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
      "available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean | Whether Middesk's TIN Match service is currently available. |

## Native endpoint

Through the native Middesk API, this operation is `GET /tin_match/availability` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tin-match-availability.md) for the provider-specific parameters and requirements.

