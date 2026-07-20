# CueGrowth: List Connections



```
GET https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-connections?${params}`, {
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
| `page` | number | no | Page number for pagination. |
| `pageSize` | number | no | Page size for pagination. Maximum 100. |
| `creationDateGt` | date | no | Filter connections after this ISO 8601 datetime. |
| `creationDateLt` | date | no | Filter connections before this ISO 8601 datetime. |
| `receiverUsername` | string | no | Filter connections to a receiver with this LinkedIn username. |
| `receiverFirstName` | string | no | Filter connections to a receiver with this first name. |
| `receiverLastName` | string | no | Filter connections to a receiver with this last name. |
| `campaigns` | number | no | Filter by campaign ID. |
| `users` | number | no | Filter by user ID. |
| `campaignTypes` | string | no | Filter connections by campaign type. |
| `clickedOnly` | boolean | no | Filter connections that clicked the tracking link. |
| `connectionDateLt` | date | no | Filter connections before this ISO 8601 datetime. |
| `connectionDateGt` | date | no | Filter connections after this ISO 8601 datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {
          "campaign": {
            "id": 1,
            "name": "Ava Chen",
            "type": "string"
          },
          "clicked_links": "https://example.com",
          "creation_date": "string",
          "id": 1,
          "receiver": {
            "email": "ava@example.com",
            "first_name": "Ava",
            "id": 1,
            "last_name": "Chen",
            "linkedin_url": "https://example.com",
            "username": "Ava Chen"
          },
          "update_date": "string",
          "user": {
            "email": "ava@example.com",
            "id": 1
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results[].campaign.id` | number |  |
| `results[].campaign.name` | string |  |
| `results[].campaign.type` | string |  |
| `results[].clicked_links` | string |  |
| `results[].creation_date` | string |  |
| `results[].id` | number |  |
| `results[].receiver.email` | string |  |
| `results[].receiver.first_name` | string |  |
| `results[].receiver.id` | number |  |
| `results[].receiver.last_name` | string |  |
| `results[].receiver.linkedin_url` | string |  |
| `results[].receiver.username` | string |  |
| `results[].update_date` | string |  |
| `results[].user.email` | string |  |
| `results[].user.id` | number |  |

## Native endpoint

Through the native CueGrowth API, this operation is `GET /connections` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connections.md) for the provider-specific parameters and requirements.

