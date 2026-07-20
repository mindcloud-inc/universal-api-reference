# Gorgias: Retrieve Job

Retrieves a job from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-job?${params}`, {
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
| `id` | string | yes | Job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_datetime": "string",
      "id": 1,
      "meta": {},
      "name": "Ava Chen",
      "status": "string",
      "updated_datetime": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_datetime` | string |  |
| `id` | number |  |
| `meta` | object |  |
| `name` | string |  |
| `status` | string |  |
| `updated_datetime` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /jobs/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-job.md) for the provider-specific parameters and requirements.

