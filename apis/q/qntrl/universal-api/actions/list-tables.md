# Qntrl: List Tables

Retrieves tables from Qntrl.

```
GET https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qntrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-tables?${params}`, {
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
| `org_id` | string | no | Qntrl organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tables` | array<object> |  |

## Native endpoint

Through the native Qntrl API, this operation is `GET /[:org_id]/table` (base URL `https://coreapi.qntrl.com/blueprint/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

