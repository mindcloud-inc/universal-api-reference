# Rownd Data Privacy: Delete OIDC Client



```
DELETE https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/delete-oidc-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/delete-oidc-client?connectionId=$CONNECTION_ID&client=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "client": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/delete-oidc-client?${params}`, {
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
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the client was deleted. |
| `id` | string | Deleted OIDC client identifier. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `DELETE /oidc-clients/:client` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-oidc-client.md) for the provider-specific parameters and requirements.

