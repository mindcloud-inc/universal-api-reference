# Scale: List Deliveries



```
GET https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-deliveries?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-deliveries?${params}`, {
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
| `deliveredAfter` | string | no | Only return deliveries delivered after this timestamp. |
| `deliveredBefore` | string | no | Only return deliveries delivered before this timestamp. |
| `expand` | string | no | Comma-separated fields to expand in the response. |
| `projectId` | string | yes | Scale project identifier. Required in MindCloud for this action. |
| `projectName` | string | no | Optional alternative to Project ID when you want to scope by project name instead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveries": [
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
| `deliveries` | array<object> | Array of delivery objects. |

## Native endpoint

Through the native Scale API, this operation is `GET /v2/deliveries` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deliveries.md) for the provider-specific parameters and requirements.

