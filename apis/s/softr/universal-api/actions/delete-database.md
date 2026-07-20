# Softr: Delete Database



```
DELETE https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-database?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-database?${params}`, {
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
| `databaseId` | string | yes | The ID of the database. |
| `force` | boolean | no | Delete the database even when it is not empty. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databaseId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | string |  |

## Native endpoint

Through the native Softr API, this operation is `DELETE /databases/:databaseId` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-database.md) for the provider-specific parameters and requirements.

