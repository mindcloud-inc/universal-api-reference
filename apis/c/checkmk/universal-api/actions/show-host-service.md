# Checkmk: Show Host Service

Retrieves monitored service details for a Checkmk host.

```
GET https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/show-host-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/show-host-service?connectionId=$CONNECTION_ID&hostName=Ava%20Chen&serviceDescription=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostName": "Ava Chen",
  "serviceDescription": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/show-host-service?${params}`, {
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
| `hostName` | string | yes | Checkmk host name. |
| `serviceDescription` | string | yes | Exact Checkmk service description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | object |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `GET /objects/host/{host_name}/actions/show_service/invoke` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-host-service.md) for the provider-specific parameters and requirements.

