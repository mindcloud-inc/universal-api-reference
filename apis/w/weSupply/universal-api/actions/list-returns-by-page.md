# WeSupply: List Returns By Page

Retrieves a page of returns from WeSupply.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/list-returns-by-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/list-returns-by-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/list-returns-by-page?${params}`, {
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
| `page` | string | no | Page number for paginated return listings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedAt": "string",
      "Reference": "string",
      "RefundCost": 1,
      "State": "string",
      "UpdatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedAt` | string |  |
| `Reference` | string |  |
| `RefundCost` | number |  |
| `State` | string |  |
| `UpdatedAt` | string |  |

## Native endpoint

Through the native WeSupply API, this operation is `GET /returns` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-returns-by-page.md) for the provider-specific parameters and requirements.

