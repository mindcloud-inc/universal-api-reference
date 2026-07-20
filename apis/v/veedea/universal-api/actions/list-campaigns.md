# Veedea: List Campaigns

Retrieves all campaign records from Veedea.

```
GET https://connect.mindcloud.co/v1/universal/veedea/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veedea `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veedea/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veedea/latest/actions/list-campaigns?${params}`, {
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
| `token` | string | yes | Auth token returned by the Veedea authentication endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campName": "Ava Chen",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campName` | string | Campaign name. |
| `id` | number | Campaign ID. |

## Native endpoint

Through the native Veedea API, this operation is `GET /getcampaign` (base URL `https://veedea.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

