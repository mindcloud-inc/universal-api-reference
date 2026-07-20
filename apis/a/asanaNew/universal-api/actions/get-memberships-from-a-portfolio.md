# Asana: Get memberships from a portfolio

Retrieves portfolio memberships from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-portfolio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-portfolio?connectionId=$CONNECTION_ID&limit=25&offset=0&portfolioGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "portfolioGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-portfolio?${params}`, {
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
| `portfolioGid` | string | yes | Asana portfolio gid parameter. |
| `user` | string | no | Asana user parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `limit` | number | no | Asana limit parameter. |
| `offset` | string | no | Asana offset parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "gid": "string",
      "portfolio": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "resourceType": "string",
      "user": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `gid` | string |  |
| `portfolio.gid` | string |  |
| `portfolio.name` | string |  |
| `portfolio.resourceType` | string |  |
| `resourceType` | string |  |
| `user.gid` | string |  |
| `user.name` | string |  |
| `user.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET portfolios/:portfolio_gid/portfolio_memberships` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-memberships-from-a-portfolio.md) for the provider-specific parameters and requirements.

