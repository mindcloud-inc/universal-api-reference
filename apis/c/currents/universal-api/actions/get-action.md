# Currents: Get Action



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-action?connectionId=$CONNECTION_ID&actionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-action?${params}`, {
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
| `actionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "actionId": "string",
        "createdAt": "string",
        "cursor": "string",
        "name": "Ava Chen"
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
| `data.actionId` | string |  |
| `data.createdAt` | string |  |
| `data.cursor` | string |  |
| `data.name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /actions/:actionId` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

