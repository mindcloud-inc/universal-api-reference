# InflatableOffice: Get Worker

Retrieves a worker from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-worker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-worker?connectionId=$CONNECTION_ID&workerId=13687" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workerId": "13687"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-worker?${params}`, {
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
| `workerId` | number | yes | Worker ID to retrieve. Example: `13687`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": "string",
      "cphone": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "href": "string",
      "id": "string",
      "lastname": "Chen",
      "name": "Ava Chen",
      "positions": [
        "string"
      ],
      "state": "string",
      "wuname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | string |  |
| `cphone` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `href` | string |  |
| `id` | string |  |
| `lastname` | string |  |
| `name` | string |  |
| `positions[]` | string |  |
| `state` | string |  |
| `wuname` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /workers/:workerId` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-worker.md) for the provider-specific parameters and requirements.

