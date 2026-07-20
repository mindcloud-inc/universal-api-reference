# Sertifier: Delete Credential

Deletes an existing credential from Sertifier.

```
DELETE https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/delete-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/delete-credential?connectionId=$CONNECTION_ID&credential_id=Credential%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credential_id": "Credential ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/delete-credential?${params}`, {
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
| `credential_id` | string | yes | Example: `Credential ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "data": true,
      "hasError": true,
      "isUpgraded": true,
      "message": "string",
      "showPurchaseSheet": true,
      "upgradePlan": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `data` | boolean |  |
| `hasError` | boolean |  |
| `isUpgraded` | boolean |  |
| `message` | string |  |
| `showPurchaseSheet` | boolean |  |
| `upgradePlan` | object |  |

## Native endpoint

Through the native Sertifier API, this operation is `DELETE /credential/:credential_id` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-credential.md) for the provider-specific parameters and requirements.

