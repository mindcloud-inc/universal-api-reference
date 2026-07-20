# Zubie: List Subscriptions

Retrieves subscriptions from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-subscriptions?${params}`, {
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
| `cursor` | string | no | Cursor for pagination. |
| `size` | string | no | Number of results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ends_at": "string",
      "plan": {},
      "quantity": 1,
      "started_at": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ends_at` | string |  |
| `plan` | object |  |
| `quantity` | number |  |
| `started_at` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /subscriptions` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

