# Halo Service Solutions: Create Site

Creates a new site in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "client_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "client_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `client_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": 1,
      "datecreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "inactive": true,
      "maincontact_id": 1,
      "name": "Ava Chen",
      "ref": "string",
      "sla_id": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | number |  |
| `datecreated` | date |  |
| `id` | number |  |
| `inactive` | boolean |  |
| `maincontact_id` | number |  |
| `name` | string |  |
| `ref` | string |  |
| `sla_id` | number |  |
| `timezone` | string |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Site` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

