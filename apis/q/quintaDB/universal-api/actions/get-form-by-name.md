# QuintaDB: Get Form By Name

Finds a form in QuintaDB by name.

```
GET https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/get-form-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/get-form-by-name?connectionId=$CONNECTION_ID&database_name=Ava%20Chen&form_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "database_name": "Ava Chen",
  "form_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/get-form-by-name?${params}`, {
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
| `database_name` | string | yes |  |
| `form_name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `form` | object | Requested QuintaDB form found by database and name. |

## Native endpoint

Through the native QuintaDB API, this operation is `GET /apps/search/entities/search.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-by-name.md) for the provider-specific parameters and requirements.

