# BigML: Get Anomaly

Retrieves an anomaly detector from BigML.

```
GET https://connect.mindcloud.co/v1/universal/bigML/latest/actions/get-anomaly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigML `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigML/latest/actions/get-anomaly?connectionId=$CONNECTION_ID&anomalyId=69cd1234abcd1234abcd1234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "anomalyId": "69cd1234abcd1234abcd1234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigML/latest/actions/get-anomaly?${params}`, {
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
| `anomalyId` | string | yes | BigML anomaly identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include anomaly/. Example: `69cd1234abcd1234abcd1234`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "created": "string",
      "name": "Ava Chen",
      "resource": "string",
      "status": {},
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-like response code from BigML. |
| `created` | string | Creation timestamp. |
| `name` | string | Resource display name. |
| `resource` | string | BigML resource identifier. |
| `status` | object | BigML processing status object. |
| `updated` | string | Last update timestamp. |

## Native endpoint

Through the native BigML API, this operation is `GET /anomaly/:anomalyId` (base URL `https://bigml.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-anomaly.md) for the provider-specific parameters and requirements.

