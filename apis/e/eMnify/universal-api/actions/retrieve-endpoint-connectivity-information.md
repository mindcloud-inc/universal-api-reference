# EMnify: Retrieve Endpoint Connectivity Information

Retrieves connectivity information for an endpoint from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-endpoint-connectivity-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-endpoint-connectivity-information?connectionId=$CONNECTION_ID&authToken=string&endpointId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "string",
  "endpointId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-endpoint-connectivity-information?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |
| `endpointId` | number | yes | Endpoint ID to inspect. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriber` | boolean | no | Whether to request subscriber information in the connectivity lookup. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replyTimestamp": "2026-05-07T12:00:00.000Z",
      "requestTimestamp": "2026-05-07T12:00:00.000Z",
      "subscriberInfo": {
        "error": "string",
        "success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `replyTimestamp` | date |  |
| `requestTimestamp` | date |  |
| `subscriberInfo.error` | string |  |
| `subscriberInfo.success` | boolean |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /endpoint/:endpoint_id/connectivity_info` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-endpoint-connectivity-information.md) for the provider-specific parameters and requirements.

