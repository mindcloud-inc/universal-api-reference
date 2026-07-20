# Sertifier: Update Credential

Updates an existing credential in Sertifier.

```
PUT https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credential_id": "Credential ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-credential', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credential_id": "Credential ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credential_id` | string | yes | Example: `Credential ID`. |
| `name` | string | no | Example: `Updated credential recipient name`. |
| `issueDate` | date | no |  |
| `expireDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `PUT /credential/:credential_id` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-credential.md) for the provider-specific parameters and requirements.

