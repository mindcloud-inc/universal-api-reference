# Firebolt: Grant Privileges

Creates privilege grants in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/grant-privileges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/grant-privileges" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
  "privilege": "USAGE",
  "objectType": "DATABASE",
  "objectName": "mc_fb_act_20260422_db",
  "roleName": "analyst_role"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/grant-privileges', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
    "privilege": "USAGE",
    "objectType": "DATABASE",
    "objectName": "mc_fb_act_20260422_db",
    "roleName": "analyst_role"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | The Firebolt system engine host to send the SQL request to. Example: `01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io`. |
| `privilege` | string | yes | The Firebolt privilege to grant, for example USAGE or SELECT. Example: `USAGE`. |
| `objectType` | string | yes | The Firebolt object type to grant against, for example DATABASE, SCHEMA, or TABLE. Example: `DATABASE`. |
| `objectName` | string | yes | The Firebolt object name to grant against. Example: `mc_fb_act_20260422_db`. |
| `roleName` | string | yes | The Firebolt role name receiving the privilege. Example: `analyst_role`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `containerObjectType` | string | no | Optional Firebolt parent object type used in the IN clause, for example DATABASE or SCHEMA. Example: `DATABASE`. |
| `containerObjectName` | string | no | Optional Firebolt parent object name used in the IN clause. Example: `analytics`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": [
        {}
      ],
      "query": {},
      "rows": 1,
      "statistics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned data rows. |
| `meta` | array<object> | Column metadata for the response. |
| `query` | object | Firebolt query metadata. |
| `rows` | number | Number of rows returned in the data payload. |
| `statistics` | object | Firebolt execution statistics. |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/grant-privileges.md) for the provider-specific parameters and requirements.

