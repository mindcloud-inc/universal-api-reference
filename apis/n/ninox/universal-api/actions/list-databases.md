# Ninox: List Databases

Retrieves multiple databases from Ninox.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-databases?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-databases?${params}`, {
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
| `teamId` | string | yes | Workspace ID that owns the databases. Example: `YcHTn3ir8XNSp5EXK`. |

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
| `id` | string | Database ID. |
| `name` | string | Database name. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamid/databases` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.

