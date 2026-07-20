# Hy.page: List Touchpoints



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-touchpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-touchpoints?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-touchpoints?${params}`, {
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
| `id` | string | yes | Person ID whose touchpoints should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "keyword": "string",
      "landingPath": "string",
      "referrer": "string",
      "source": "string",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string",
      "utmTerm": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `keyword` | string |  |
| `landingPath` | string |  |
| `referrer` | string |  |
| `source` | string |  |
| `utmCampaign` | string |  |
| `utmContent` | string |  |
| `utmMedium` | string |  |
| `utmSource` | string |  |
| `utmTerm` | string |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/people/:id/touchpoints` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-touchpoints.md) for the provider-specific parameters and requirements.

