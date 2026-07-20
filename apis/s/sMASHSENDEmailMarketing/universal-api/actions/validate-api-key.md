# SMASHSEND Email Marketing: Validate API Key

Validates a SMASHSEND API key and returns its details.

```
GET https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/validate-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMASHSEND Email Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/validate-api-key?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Workspace or account display name associated with the API key. |
| `role` | string | Role granted to the validated API key. |
| `status` | string | Outcome of the API key validation request. |

## Native endpoint

Through the native SMASHSEND Email Marketing API, this operation is `GET /v1/api-keys/check` (base URL `https://api.smashsend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-api-key.md) for the provider-specific parameters and requirements.

