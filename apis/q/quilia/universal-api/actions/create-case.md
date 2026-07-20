# Quilia: Create Case



```
POST https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-case" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-case', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client_id` | string | no | The ID of an existing client |
| `cms_type` | string | no | Look up integration by CMS type when ID is absent |
| `native_id` | string | no | The native ID of the case in the external system. Used for integration and idempotency. |
| `new_client` | object | no | The client to associate with the case |
| `new_client.email` | string | no | The email of the client |
| `new_client.language_code` | string | no | The language code of the client |
| `new_client.name` | string | no | The name of the client |
| `new_client.name_first` | string | no | The first name of the client |
| `new_client.name_last` | string | no | The last name of the client |
| `new_client.phone` | string | no | The phone number of the client |
| `organization_integration_id` | string | no | The ID of the organization integration to use |
| `phase` | string | no | The current phase of the case |
| `type` | string | yes | The type of the case. Can be a Quilia case type or a custom CMS case type that will be mapped via integration settings. |
| `status` | list<string> | no | The status of the case One of: `closed`, `open`, `pending`. |
| `opened_at` | date | no | The date and time when the case was opened |
| `created_at` | date | no | The date and time when the case was created |
| `updated_at` | date | no | The date and time when the case was last updated |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `POST cases` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-case.md) for the provider-specific parameters and requirements.

