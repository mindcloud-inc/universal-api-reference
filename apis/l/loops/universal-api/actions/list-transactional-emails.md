# Loops: List Transactional Emails

Retrieves transactional emails from your Loops account.

```
GET https://connect.mindcloud.co/v1/universal/loops/latest/actions/list-transactional-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loops/latest/actions/list-transactional-emails?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loops/latest/actions/list-transactional-emails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "dataVariables": [
        "string"
      ],
      "id": "string",
      "lastUpdated": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataVariables` | array<string> | Template data variable names accepted by this transactional email. |
| `id` | string | Transactional email ID. |
| `lastUpdated` | string | Last updated timestamp returned by Loops. |
| `name` | string | Transactional email name. |

## Native endpoint

Through the native Loops API, this operation is `GET /transactional` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactional-emails.md) for the provider-specific parameters and requirements.

