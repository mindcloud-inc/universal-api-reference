# Chargeblast: Fetch Descriptors

Retrieves descriptors from Chargeblast.

```
GET https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-descriptors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeblast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-descriptors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-descriptors?${params}`, {
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
      "descriptors": [
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
| `descriptors` | array<object> | The descriptors associated with the current Chargeblast account. |

## Native endpoint

Through the native Chargeblast API, this operation is `GET /api/descriptors` (base URL `https://api.chargeblast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-descriptors.md) for the provider-specific parameters and requirements.

