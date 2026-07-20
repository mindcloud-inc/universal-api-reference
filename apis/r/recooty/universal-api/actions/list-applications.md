# Recooty: List Applications



```
GET https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recooty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-applications?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-applications?${params}`, {
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
| `jobId` | string | yes | The Recooty job ID. |
| `page` | string | no | The page number to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applications": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applications` | object | Paginated application collection for the requested job. |

## Native endpoint

Through the native Recooty API, this operation is `GET /v1/jobs/{{jobId}}/applications` (base URL `https://standaloneapi.recooty.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

