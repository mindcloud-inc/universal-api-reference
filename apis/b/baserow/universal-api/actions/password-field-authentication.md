# Baserow: Password Field Authentication

Checks a Baserow row against a password field.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/password-field-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/password-field-authentication?connectionId=$CONNECTION_ID&fieldId=1&rowId=1&password=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "1",
  "rowId": "1",
  "password": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/password-field-authentication?${params}`, {
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
| `fieldId` | number | yes | The password field to check. |
| `rowId` | number | yes | The row containing the password value. |
| `password` | string | yes | The password to validate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baserow API returns.

## Native endpoint

Through the native Baserow API, this operation is `POST /api/database/fields/password-authentication/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/password-field-authentication.md) for the provider-specific parameters and requirements.

