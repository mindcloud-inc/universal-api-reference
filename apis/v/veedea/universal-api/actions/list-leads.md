# Veedea: List Leads

Retrieves all lead records from Veedea.

```
GET https://connect.mindcloud.co/v1/universal/veedea/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veedea `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veedea/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=1&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "1",
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veedea/latest/actions/list-leads?${params}`, {
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
| `campaignId` | number | yes | Campaign ID returned by the Veedea campaigns endpoint. |
| `token` | string | yes | Auth token returned by the Veedea authentication endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campid": "string",
      "device": "string",
      "id": 1,
      "region": "string",
      "registerDate": "string",
      "source": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campid` | string | Campaign identifier returned in each lead row. |
| `device` | string | Lead device. |
| `id` | number | Lead record ID. |
| `region` | string | Lead region. |
| `registerDate` | string | Lead registration timestamp. |
| `source` | string | Lead source. |
| `userEmail` | string | Lead email address. |
| `userName` | string | Lead user name. |

## Native endpoint

Through the native Veedea API, this operation is `GET /getleads` (base URL `https://veedea.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

