# GetResponse: List Newsletters

Retrieves a list of newsletters from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-newsletters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-newsletters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-newsletters?${params}`, {
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
| `subject` | string | no | Filter newsletters by subject |
| `name` | string | no | Filter newsletters by name |
| `status` | string | no | Filter newsletters by status |
| `type` | string | no | Filter newsletters by type |
| `campaignId` | string | no | Filter newsletters by campaign |
| `createdOnFrom` | string | no | Return newsletters created on or after this date |
| `createdOnTo` | string | no | Return newsletters created on or before this date |
| `sendOnFrom` | string | no | Return newsletters scheduled on or after this date |
| `sendOnTo` | string | no | Return newsletters scheduled on or before this date |
| `sortCreatedOn` | string | no | Sort newsletters by creation date |
| `sortSendOn` | string | no | Sort newsletters by send date |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "newsletterId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `newsletterId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /newsletters` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-newsletters.md) for the provider-specific parameters and requirements.

