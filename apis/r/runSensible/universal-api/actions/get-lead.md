# RunSensible: Get Lead



```
GET https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSensible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-lead?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-lead?${params}`, {
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
| `id` | string | yes | The lead identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `name` | string |  |

## Native endpoint

Through the native RunSensible API, this operation is `GET /api/Lead/Get` (base URL `https://app.runsensible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

