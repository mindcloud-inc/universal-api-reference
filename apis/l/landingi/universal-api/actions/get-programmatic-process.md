# Landingi: Get Programmatic Process

Retrieves a programmatic process from Landingi by UUID.

```
GET https://connect.mindcloud.co/v1/universal/landingi/latest/actions/get-programmatic-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landingi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/get-programmatic-process?connectionId=$CONNECTION_ID&processUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landingi/latest/actions/get-programmatic-process?${params}`, {
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
| `processUuid` | string | yes | Programmatic process UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "credits_cost": 1,
      "errors": 1,
      "identifier": "string",
      "name": "Ava Chen",
      "processed": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Process creation timestamp. |
| `credits_cost` | number | Credits consumed by the process. |
| `errors` | number | Number of landing pages that failed. |
| `identifier` | string | Programmatic process identifier. |
| `name` | string | Programmatic process name. |
| `processed` | number | Number of processed landing pages. |
| `status` | string | Current process status. |
| `total` | number | Total landing pages in the process. |

## Native endpoint

Through the native Landingi API, this operation is `GET /landing-page/programmatic/processes/:processUuid` (base URL `https://api.landingi.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-programmatic-process.md) for the provider-specific parameters and requirements.

