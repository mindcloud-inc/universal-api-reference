# Flexopus: Import Users

Imports users into Flexopus from a file.

```
POST https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/import-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/import-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/import-users', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Accepted file formats: csv, txt, ods, xls, xlsx. |
| `update` | boolean | no | Whether existing users should be updated. Default: `false`. |
| `restore` | boolean | no | Whether deactivated users present in the list should be re-activated. Default: `false`. |
| `deactivate` | boolean | no | Whether users not present in the list should be deactivated. Default: `false`. |
| `keyColumn` | list<string> | no | Column used to identify existing users during import. One of: `email`, `id`, `upn`. Default: `email`. |
| `dryRun` | boolean | no | Simulate the import without making modifications. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": [
        1
      ],
      "deleted": 1,
      "dryRun": true,
      "errorMessages": {},
      "errors": [
        1
      ],
      "filename": "Ava Chen",
      "rows": 1,
      "skipped": [
        1
      ],
      "updated": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | array<number> |  |
| `deleted` | number |  |
| `dryRun` | boolean |  |
| `errorMessages` | object |  |
| `errors` | array<number> |  |
| `filename` | string |  |
| `rows` | number |  |
| `skipped` | array<number> |  |
| `updated` | array<number> |  |

## Native endpoint

Through the native Flexopus API, this operation is `POST /users/import` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-users.md) for the provider-specific parameters and requirements.

