# Storyscale: Get Tour



```
GET https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/get-tour
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyscale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/get-tour?connectionId=$CONNECTION_ID&tourId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tourId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/get-tour?${params}`, {
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
| `tourId` | string | yes | The Storyscale tour ID. |
| `withScreens` | boolean | no | Include tour screens in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Tour payload returned by Storyscale. |
| `status` | object | Top-level API status object. |

## Native endpoint

Through the native Storyscale API, this operation is `GET /v1/tour/view/{tour_id}/` (base URL `https://prodapi.storyscale.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tour.md) for the provider-specific parameters and requirements.

