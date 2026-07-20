# Optform: List User Forms

Retrieves forms created by a specific Optform user.

```
GET https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-user-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-user-forms?connectionId=$CONNECTION_ID&userId=0e79ab5c-6229-4948-904e-dd2bcabc3dc2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "0e79ab5c-6229-4948-904e-dd2bcabc3dc2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-user-forms?${params}`, {
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
| `userId` | string | yes | Example: `0e79ab5c-6229-4948-904e-dd2bcabc3dc2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Optform API, this operation is `GET /api/Form/user/:userId` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-forms.md) for the provider-specific parameters and requirements.

