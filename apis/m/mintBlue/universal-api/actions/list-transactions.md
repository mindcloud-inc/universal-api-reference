# mintBlue: List Transactions

Retrieves transactions from mintBlue.

```
GET https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-transactions?connectionId=$CONNECTION_ID&params.project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-transactions?${params}`, {
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
| `params.project_id` | string | yes | Project ID filter (required for stable results in this account). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.startDate` | date | no | Optional start date filter. |
| `params.endDate` | date | no | Optional end date filter. |
| `params.sort` | string | no | Optional sort field. |
| `params.order` | string | no | Optional sort order (asc\|desc). |
| `params.paginationOptions.limit` | number | no | Optional pagination limit. |
| `params.paginationOptions.offset` | number | no | Optional pagination offset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block": 1,
      "confirmed_at": "string",
      "count": "string",
      "created_at": "string",
      "metadata": {},
      "privdata": {},
      "project_id": "string",
      "published_at": "string",
      "size": 1,
      "status": "string",
      "txid": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | number |  |
| `confirmed_at` | string |  |
| `count` | string |  |
| `created_at` | string |  |
| `metadata` | object |  |
| `privdata` | object |  |
| `project_id` | string |  |
| `published_at` | string |  |
| `size` | number |  |
| `status` | string |  |
| `txid` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

