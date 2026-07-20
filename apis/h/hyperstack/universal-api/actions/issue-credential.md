# Hyperstack Certificates: Issue Credential



```
POST https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/issue-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/issue-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "custom_attributes": {},
  "group_key": "string",
  "recipient": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/issue-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "custom_attributes": {},
    "group_key": "string",
    "recipient": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom_attributes` | object | yes | Custom credential attributes keyed by custom_-prefixed field names. |
| `group_key` | string | yes | The credential group key to issue into. |
| `recipient` | object | yes | Recipient object containing name and email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "document_url": "https://example.com",
      "group": {},
      "issued_on": "string",
      "metadata": {},
      "privacy": "string",
      "recipient": {},
      "status": "string",
      "success": true,
      "valid_until": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | string | The unique ID of the newly created credential. |
| `document_url` | string | URL to view the newly created credential. |
| `group` | object | Credential group summary for the issued credential. |
| `issued_on` | string | ISO 8601 timestamp when the credential was issued. |
| `metadata` | object | Custom attribute values stored with the credential. |
| `privacy` | string | Credential visibility. |
| `recipient` | object | Recipient object with name and email. |
| `status` | string | Publication status of the credential. |
| `success` | boolean | Indicates whether the credential was successfully issued. |
| `valid_until` | string | ISO 8601 expiry timestamp if present. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /credentials/new` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-credential.md) for the provider-specific parameters and requirements.

