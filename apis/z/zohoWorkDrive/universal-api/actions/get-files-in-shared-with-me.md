# Zoho WorkDrive: Get Files in Shared with Me

Retrieves files shared with a Zoho WorkDrive user.

```
GET https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-files-in-shared-with-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho WorkDrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-files-in-shared-with-me?connectionId=$CONNECTION_ID&limit=25&offset=0&teamMemberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teamMemberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-files-in-shared-with-me?${params}`, {
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
| `teamMemberId` | string | yes | The team member ID. |
| `filterType` | string | no | Filter the results by resource type. |
| `filterUser` | string | no | Filter by the sharing user. |
| `filterGroup` | string | no | Filter by the sharing group. |
| `limit` | string | no | Maximum number of records to return. |
| `offset` | string | no | Number of records to skip before returning results. |
| `sort` | string | no | Sort expression for the returned resources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Provider resource attributes. |
| `id` | string | Resource ID. |
| `links` | object | Provider self and related links. |
| `relationships` | object | Provider relationship links. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Zoho WorkDrive API, this operation is `GET /api/v1/users/:teamMemberId/incomingfiles` (base URL `{{credentials.accessTokenRequest.api_domain}}/workdrive`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-files-in-shared-with-me.md) for the provider-specific parameters and requirements.

