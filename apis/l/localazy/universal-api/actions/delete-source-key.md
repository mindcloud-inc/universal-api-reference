# Localazy: Delete Source Key

Deletes an existing source key from Localazy.

```
DELETE https://connect.mindcloud.co/v1/universal/localazy/latest/actions/delete-source-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/delete-source-key?connectionId=$CONNECTION_ID&projectId=string&keyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "keyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/delete-source-key?${params}`, {
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
| `projectId` | string | yes | Localazy project id or slug. |
| `keyId` | string | yes | Source key identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean | Whether the source key was deleted successfully. |

## Native endpoint

Through the native Localazy API, this operation is `DELETE /projects/:projectId/keys/:keyId` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-source-key.md) for the provider-specific parameters and requirements.

