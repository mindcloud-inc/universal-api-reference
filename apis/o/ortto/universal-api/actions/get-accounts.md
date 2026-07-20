# Ortto: Get Accounts



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-accounts?connectionId=$CONNECTION_ID&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-accounts?${params}`, {
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
| `fields[]` | array<string> | yes | Account field IDs to return, such as str::name. |
| `limit` | number | no | Maximum number of accounts to return. |
| `offset` | number | no | Number of accounts to skip. |
| `sortByFieldId` | string | no | Account field ID to sort by. |
| `sortOrder` | string | no | Sort direction. |
| `q` | string | no | Search accounts by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {
          "fields": {
            "str:o:name": "Ava Chen"
          },
          "id": "string"
        }
      ],
      "cursorId": "string",
      "hasMore": true,
      "meta": {
        "totalContacts": 1,
        "totalMatches": 1,
        "totalOrganizations": 1,
        "totalSubscribers": 1
      },
      "nextOffset": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[].fields.str:o:name` | string |  |
| `accounts[].id` | string |  |
| `cursorId` | string |  |
| `hasMore` | boolean |  |
| `meta.totalContacts` | number |  |
| `meta.totalMatches` | number |  |
| `meta.totalOrganizations` | number |  |
| `meta.totalSubscribers` | number |  |
| `nextOffset` | number |  |
| `offset` | number |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /accounts/get` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-accounts.md) for the provider-specific parameters and requirements.

