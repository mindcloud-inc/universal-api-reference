# Société.com: List Company Financial Statements

Retrieves company financial statements from Société.com.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/list-company-financial-statements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/list-company-financial-statements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/list-company-financial-statements?${params}`, {
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
| `numid` | string | no | Company identifier or SIREN. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bilans": [
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
| `bilans` | array<object> | Financial statement entries available for the company. |

## Native endpoint

Through the native Société.com API, this operation is `GET /entreprise/:numid/bilans` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-financial-statements.md) for the provider-specific parameters and requirements.

