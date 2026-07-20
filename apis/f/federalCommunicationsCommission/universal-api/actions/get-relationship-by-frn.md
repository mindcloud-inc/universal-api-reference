# Federal Communications Commission: Get Relationship by FRN

Retrieves FCC relationships by FRN.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-relationship-by-frn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-relationship-by-frn?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-relationship-by-frn?${params}`, {
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
| `frn` | string | no | FCC Registration Number; documented as 10 digits. |

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

Through the native Federal Communications Commission API, this operation is `GET /api/service/relationship/frn/{frn}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-relationship-by-frn.md) for the provider-specific parameters and requirements.

