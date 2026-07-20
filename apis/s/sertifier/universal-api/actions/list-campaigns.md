# Sertifier: List Campaigns

Finds campaigns in Sertifier by search filters.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-campaigns?${params}`, {
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
| `startIndex` | number | no | Default: `0`. |
| `length` | number | no | Default: `10`. |
| `status[]` | array<number> | no | Accepts multiple values as an array. Example: `1,2,3`. |
| `searchTerm` | string | no | Example: `campaign title`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeId": {},
      "createDate": "string",
      "designId": "string",
      "detailId": "string",
      "emailFromAddress": "ava@example.com",
      "emailFromName": "ava@example.com",
      "emailSubject": "ava@example.com",
      "emailTemplateId": "ava@example.com",
      "id": "string",
      "privateCampaign": true,
      "status": 1,
      "title": "string",
      "updateDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeId` | object |  |
| `createDate` | string |  |
| `designId` | string |  |
| `detailId` | string |  |
| `emailFromAddress` | string |  |
| `emailFromName` | string |  |
| `emailSubject` | string |  |
| `emailTemplateId` | string |  |
| `id` | string |  |
| `privateCampaign` | boolean |  |
| `status` | number |  |
| `title` | string |  |
| `updateDate` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /campaign/search` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

