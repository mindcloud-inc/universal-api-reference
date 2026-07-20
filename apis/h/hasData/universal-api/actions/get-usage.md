# HasData: Get Usage

Retrieves HasData usage and concurrency details.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-usage?${params}`, {
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
        "availableConcurrency": 1,
        "availableCredits": 1,
        "totalConcurrency": 1,
        "totalCredits": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.availableConcurrency` | number | Remaining available concurrency. |
| `data.availableCredits` | number | Remaining available credits. |
| `data.totalConcurrency` | number | Current concurrent requests in use. |
| `data.totalCredits` | number | Total account credits. |
| `status` | string | HasData request status. |

## Native endpoint

Through the native HasData API, this operation is `GET /user/me/usage` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

