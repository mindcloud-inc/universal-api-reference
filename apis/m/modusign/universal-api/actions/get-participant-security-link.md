# Modusign: Get Participant Security Link

Retrieves a participant security link from Modusign.

```
GET https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-participant-security-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-participant-security-link?connectionId=$CONNECTION_ID&documentId=string&participantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "participantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-participant-security-link?${params}`, {
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
| `documentId` | string | yes | The Modusign document ID. |
| `participantId` | string | yes | The Modusign participant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "securityLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `securityLink` | string | The participant security link URL. |

## Native endpoint

Through the native Modusign API, this operation is `GET /documents/:documentId/participants/:participantId/security-link` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-participant-security-link.md) for the provider-specific parameters and requirements.

