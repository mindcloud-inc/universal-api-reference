# Intelliprint: List Mailing List Recipients



```
GET https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/list-mailing-list-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/list-mailing-list-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0&mailingList=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "mailingList": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/list-mailing-list-recipients?${params}`, {
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
| `mailingList` | string | yes | The Intelliprint mailing list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "has_more": true,
      "object": "string",
      "total_available": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `has_more` | boolean |  |
| `object` | string |  |
| `total_available` | number |  |

## Native endpoint

Through the native Intelliprint API, this operation is `GET /mailing_lists/:mailingList/recipients` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mailing-list-recipients.md) for the provider-specific parameters and requirements.

