# Xola: Get Batch Availability

Retrieves batch availability from Xola.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/get-batch-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/get-batch-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/get-batch-availability?${params}`, {
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
      "availabilityByExperience": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityByExperience` | object | Availability map keyed by experience identifier. |

## Native endpoint

Through the native Xola API, this operation is `GET /availability` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-availability.md) for the provider-specific parameters and requirements.

