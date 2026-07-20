# Leiga: Get Sprint

Retrieves detailed sprint information from Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-sprint?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-sprint?${params}`, {
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
| `id` | number | yes | Sprint ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": 1,
      "goal": "string",
      "id": 1,
      "name": "Ava Chen",
      "startDate": 1,
      "started": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | number |  |
| `goal` | string |  |
| `id` | number |  |
| `name` | string |  |
| `startDate` | number |  |
| `started` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Leiga API, this operation is `GET /sprint/get` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sprint.md) for the provider-specific parameters and requirements.

