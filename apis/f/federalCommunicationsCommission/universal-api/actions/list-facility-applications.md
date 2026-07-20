# Federal Communications Commission: List Facility Applications

Retrieves FCC facility applications by entity ID.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-facility-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-facility-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-facility-applications?${params}`, {
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
| `entityId` | string | no | FCC entity or facility ID. |
| `serviceType` | string | no | Service type. FCC documents tv, fm, am, cable, sdars, dbs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "responseTime": 1,
      "results": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | FCC service response message. |
| `responseTime` | number | FCC service response time. |
| `results` | object | Endpoint-specific FCC result payload. |
| `status` | string | FCC service response status. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/service/{serviceType}/applications/facility/{entityID}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-facility-applications.md) for the provider-specific parameters and requirements.

