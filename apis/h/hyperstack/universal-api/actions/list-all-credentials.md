# Hyperstack Certificates: List All Credentials



```
GET https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/list-all-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/list-all-credentials?connectionId=$CONNECTION_ID&page=1&page_size=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "1",
  "page_size": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/list-all-credentials?${params}`, {
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
| `page` | number | yes | The page number for pagination. Default: `1`. |
| `page_size` | number | yes | The number of credentials to return per page. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "documentUrl": "https://example.com",
      "group": {},
      "issuedOn": "string",
      "metadata": {},
      "privacy": "string",
      "recipient": {},
      "status": "string",
      "validUntil": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | Credential document identifier. |
| `documentUrl` | string | Public URL for the credential. |
| `group` | object | Credential group summary. |
| `issuedOn` | string | ISO timestamp when the credential was issued. |
| `metadata` | object | Additional credential metadata. |
| `privacy` | string | Credential visibility mode. |
| `recipient` | object | Recipient identity for the credential. |
| `status` | string | Credential lifecycle status. |
| `validUntil` | string | ISO timestamp when the credential expires, if any. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /credentials/all` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-credentials.md) for the provider-specific parameters and requirements.

