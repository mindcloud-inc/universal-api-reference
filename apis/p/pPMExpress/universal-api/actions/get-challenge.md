# PPM Express: Get Challenge



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-challenge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-challenge?connectionId=$CONNECTION_ID&id=5db46250-3468-40f8-ae12-411ffe16b58f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "5db46250-3468-40f8-ae12-411ffe16b58f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-challenge?${params}`, {
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
| `id` | string | yes | The challenge ID to fetch. Default: `5db46250-3468-40f8-ae12-411ffe16b58f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The requested challenge record. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/challenges/:id` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-challenge.md) for the provider-specific parameters and requirements.

