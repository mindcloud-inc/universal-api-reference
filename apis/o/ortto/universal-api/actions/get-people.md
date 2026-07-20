# Ortto: Get People



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-people?connectionId=$CONNECTION_ID&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-people?${params}`, {
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
| `fields[]` | array<string> | yes | Person field IDs to return, such as str::email. |
| `limit` | number | no | Maximum number of people to return. |
| `offset` | number | no | Number of people to skip before returning results. |
| `sortByFieldId` | string | no | Field ID to sort people by. |
| `sortOrder` | string | no | Sort order for returned people: asc or desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "fields": {
            "str::email": "ava@example.com",
            "str::first": "string",
            "str::last": "string"
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
| `contacts[].fields.str::email` | string |  |
| `contacts[].fields.str::first` | string |  |
| `contacts[].fields.str::last` | string |  |
| `contacts[].id` | string |  |
| `cursorId` | string |  |
| `hasMore` | boolean |  |
| `meta.totalContacts` | number |  |
| `meta.totalMatches` | number |  |
| `meta.totalOrganizations` | number |  |
| `meta.totalSubscribers` | number |  |
| `nextOffset` | number |  |
| `offset` | number |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /person/get` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-people.md) for the provider-specific parameters and requirements.

