# Chargback: List Business Accounts



```
GET https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-business-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-business-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-business-accounts?${params}`, {
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
| `page` | number | no |  |
| `page_size` | number | no |  |
| `ordered_by` | string | no |  |
| `name` | string | no |  |
| `is_active` | boolean | no |  |
| `base_currency` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number | Total number of business accounts available for the current credential. |
| `next` | string | Next-page URL when the provider has more results. |
| `previous` | string | Previous-page URL when the current page is not the first page. |
| `results` | array<object> | List of business-account records returned by Chargeback. |

## Native endpoint

Through the native Chargback API, this operation is `GET /api/public/v1/business_accounts/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-accounts.md) for the provider-specific parameters and requirements.

