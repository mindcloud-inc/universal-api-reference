# Qntrl: Get Row Details

Retrieves row details from a Qntrl table.

```
GET https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-row-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qntrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-row-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-row-details?${params}`, {
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
| `row_id` | string | no | Qntrl row ID. |
| `table_id` | string | no | Qntrl table ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "rowId": "string",
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string |  |
| `rowId` | string |  |
| `values` | object |  |

## Native endpoint

Through the native Qntrl API, this operation is `GET /[:org_id]/table/[:table_id]/row/[:row_id]` (base URL `https://coreapi.qntrl.com/blueprint/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-row-details.md) for the provider-specific parameters and requirements.

