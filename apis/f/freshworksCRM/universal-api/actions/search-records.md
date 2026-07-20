# Freshworks CRM: Search Records

Finds matching records in Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/search-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/search-records?${params}`, {
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
| `include` | string | no | Comma-separated models to include (for example: contact,lead,sales_account,deal). |
| `q` | string | no | Text query to search for records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "avatar": "string",
          "country": "string",
          "email": "ava@example.com",
          "id": "string",
          "mcr_id": 1,
          "name": "Ava Chen",
          "owner": {
            "id": 1,
            "name": "Ava Chen"
          },
          "primary_sales_account_name": "Ava Chen",
          "type": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "website": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].avatar` | string |  |
| `[].country` | string |  |
| `[].email` | string |  |
| `[].id` | string |  |
| `[].mcr_id` | number |  |
| `[].name` | string |  |
| `[].owner.id` | number |  |
| `[].owner.name` | string |  |
| `[].primary_sales_account_name` | string |  |
| `[].type` | string |  |
| `[].updated_at` | date |  |
| `[].website` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/search` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

