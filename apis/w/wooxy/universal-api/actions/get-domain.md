# Wooxy: Get Domain

Retrieves a domain from your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-domain?${params}`, {
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
| `domainId` | string | no | The Wooxy domain ID. Use this or Domain. Example: `69d68b03cab91f1ed601af02`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | The registered domain name. Use this or Domain ID. Example: `stage3-20260408.example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "domain": "string",
        "domainId": "string",
        "isTrial": true
      },
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.domain` | string |  |
| `data.domainId` | string |  |
| `data.isTrial` | boolean |  |
| `errors` | array<string> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/domain/get` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

