# Verix: Delete Credential

Deletes an unissued credential from Verix.

```
DELETE https://connect.mindcloud.co/v1/universal/verix/latest/actions/delete-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/verix/latest/actions/delete-credential?connectionId=$CONNECTION_ID&credential_id=3145dfc827ed4c95aa6c5f2b80ac4008" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credential_id": "3145dfc827ed4c95aa6c5f2b80ac4008"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verix/latest/actions/delete-credential?${params}`, {
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
| `credential_id` | string | yes | Credential ID to delete. Example: `3145dfc827ed4c95aa6c5f2b80ac4008`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Provider error or status code. |
| `message` | string | Provider response message. |

## Native endpoint

Through the native Verix API, this operation is `DELETE /v1/credentials/:credential_id/` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-credential.md) for the provider-specific parameters and requirements.

