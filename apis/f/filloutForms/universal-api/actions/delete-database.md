# Fillout Forms: Delete Database

Deletes a database from Fillout.

```
DELETE https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-database?connectionId=$CONNECTION_ID&databaseId=bad4b276-f604-47ad-86e5-d2ae4f60968f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "bad4b276-f604-47ad-86e5-d2ae4f60968f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-database?${params}`, {
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
| `databaseId` | string | yes | The unique identifier of the database Example: `bad4b276-f604-47ad-86e5-d2ae4f60968f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the database was deleted. |

## Native endpoint

Through the native Fillout Forms API, this operation is `DELETE https://tables.fillout.com/api/v1/bases/:databaseId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-database.md) for the provider-specific parameters and requirements.

