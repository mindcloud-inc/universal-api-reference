# Didit: Retrieve Session

Retrieves a session decision from Didit.

```
GET https://connect.mindcloud.co/v1/universal/didit/latest/actions/retrieve-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/didit/latest/actions/retrieve-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/retrieve-session?${params}`, {
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
| `sessionId` | string | yes | Didit session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sessionId": "string",
      "status": "string",
      "vendorData": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sessionId` | string |  |
| `status` | string |  |
| `vendorData` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Didit API, this operation is `GET https://verification.didit.me/v3/session/{sessionId}/decision/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-session.md) for the provider-specific parameters and requirements.

