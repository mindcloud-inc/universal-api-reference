# E2B: Get Build Status

Retrieves template build status from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-status?connectionId=$CONNECTION_ID&buildId=string&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "string",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-status?${params}`, {
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
| `buildId` | string | yes | Identifier of the template build. |
| `templateId` | string | yes | Identifier of the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buildID": "string",
      "logs": [
        {}
      ],
      "reason": {},
      "status": "string",
      "templateID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildID` | string | Identifier of the build. |
| `logs` | array<object> | Build logs included with build status. |
| `reason` | object | Status reason details. |
| `status` | string | Build status. |
| `templateID` | string | Identifier of the template. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates/{templateID}/builds/{buildID}/status` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build-status.md) for the provider-specific parameters and requirements.

