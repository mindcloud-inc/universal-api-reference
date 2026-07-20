# CrewMem: Get Memory Job



```
GET https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/get-memory-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrewMem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/get-memory-job?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/get-memory-job?${params}`, {
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
| `id` | number | yes | Memory job ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider docs expose a generic memory job payload on successful reads. |
| `success` | boolean |  |

## Native endpoint

Through the native CrewMem API, this operation is `GET /api/memory/jobs/:id` (base URL `https://crewmem.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-memory-job.md) for the provider-specific parameters and requirements.

