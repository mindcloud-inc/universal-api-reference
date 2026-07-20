# condoo: Retrieve Website Statistics

Retrieves website statistics from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-website-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-website-statistics?connectionId=$CONNECTION_ID&endDate=2026-05-07T12%3A00%3A00.000Z&startDate=2026-05-07T12%3A00%3A00.000Z&websiteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-05-07T12:00:00.000Z",
  "startDate": "2026-05-07T12:00:00.000Z",
  "websiteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-website-statistics?${params}`, {
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
| `countryCode` | string | no | Optional country code. |
| `endDate` | date | yes | Required end date. |
| `startDate` | date | yes | Required start date. |
| `type` | string | no | Optional statistics type. |
| `utmSource` | string | no | Optional UTM source for supported UTM statistics types. |
| `websiteId` | number | yes | Required website ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounces": 1,
      "pageviews": 1,
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounces` | number |  |
| `pageviews` | number |  |
| `path` | string |  |

## Native endpoint

Through the native condoo API, this operation is `GET /statistics/{website_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-website-statistics.md) for the provider-specific parameters and requirements.

