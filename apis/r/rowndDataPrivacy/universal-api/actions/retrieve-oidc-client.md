# Rownd Data Privacy: Retrieve OIDC Client



```
GET https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/retrieve-oidc-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/retrieve-oidc-client?connectionId=$CONNECTION_ID&client=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "client": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/retrieve-oidc-client?${params}`, {
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
| `client` | string | yes | Rownd OIDC client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": "string",
      "grant_types": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "redirect_uris": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string | OIDC client ID. |
| `grant_types` | array<string> | Allowed OAuth grant types. |
| `id` | string | OIDC client identifier. |
| `name` | string | OIDC client display name. |
| `redirect_uris` | array<string> | Allowed redirect URIs. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `GET /oidc-clients/:client` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-oidc-client.md) for the provider-specific parameters and requirements.

