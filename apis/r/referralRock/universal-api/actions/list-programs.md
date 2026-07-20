# Referral Rock: List Programs

Retrieves referral programs from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-programs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-programs?${params}`, {
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
| `programId` | string | no | Id of the program of interest. |
| `programId` | string | no | ID of the program of interest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "memberOffer": "string",
      "name": "Ava Chen",
      "referralOffer": "string",
      "title": "string",
      "type": "string",
      "widgetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directUrl` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `memberOffer` | string |  |
| `name` | string |  |
| `referralOffer` | string |  |
| `title` | string |  |
| `type` | string |  |
| `widgetUrl` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/programs` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-programs.md) for the provider-specific parameters and requirements.

