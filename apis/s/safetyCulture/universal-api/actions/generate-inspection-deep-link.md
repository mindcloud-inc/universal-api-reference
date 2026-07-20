# SafetyCulture: Generate Inspection Deep Link

Generates an inspection deep link in SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/generate-inspection-deep-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/generate-inspection-deep-link?connectionId=$CONNECTION_ID&auditId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/generate-inspection-deep-link?${params}`, {
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
| `auditId` | string | yes | The id of the inspection to retrieve a deep link for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /audits/{audit_id}/deep_link` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-inspection-deep-link.md) for the provider-specific parameters and requirements.

