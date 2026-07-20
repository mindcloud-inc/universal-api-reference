# Kiwili: Create Project

Creates a new project in Kiwili.

```
POST https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "EnterpriseId": 1,
  "Name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "EnterpriseId": 1,
    "Name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the project is active. |
| `EnterpriseId` | number | yes | The client enterprise ID for the project. |
| `Name` | string | yes | The project name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Archive": true,
      "EnterpriseId": 1,
      "Id": 1,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Archive` | boolean |  |
| `EnterpriseId` | number |  |
| `Id` | number |  |
| `Name` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `POST /project` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

