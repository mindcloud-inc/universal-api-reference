# Stripo: Delete Email

Deletes an email from Stripo.

```
DELETE https://connect.mindcloud.co/v1/universal/stripo/latest/actions/delete-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/delete-email?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/delete-email?${params}`, {
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
| `id` | number | yes | The email ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | 200 OK confirmation from Stripo for the delete request. |

## Native endpoint

Through the native Stripo API, this operation is `DELETE /emails/:id` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email.md) for the provider-specific parameters and requirements.

