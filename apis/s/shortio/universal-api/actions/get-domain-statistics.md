# Short.io: Get Domain Statistics

Retrieves domain statistics from Short.io.

```
GET https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-domain-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-domain-statistics?connectionId=$CONNECTION_ID&domainId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-domain-statistics?${params}`, {
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
| `domainId` | number | yes | Domain ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser": [
        {}
      ],
      "city": [
        {}
      ],
      "clicks": 1,
      "clicksPerLink": "https://example.com",
      "clicksPerLinkChange": "https://example.com",
      "clickStatistics": {},
      "country": [
        {}
      ],
      "device": [
        {}
      ],
      "humanClicks": 1,
      "humanClicksChange": "string",
      "humanClicksChangePositive": true,
      "humanClicksPerLink": "https://example.com",
      "interval": {},
      "links": 1,
      "linksChange": "https://example.com",
      "linksChangePositive": true,
      "loading": true,
      "os": [
        {}
      ],
      "prevClicks": 1,
      "prevClicksChange": "string",
      "prevHumanClicks": 1,
      "referer": [
        {}
      ],
      "sample": true,
      "social": [
        {}
      ],
      "utmCampaign": [
        {}
      ],
      "utmContent": [
        {}
      ],
      "utmMedium": [
        {}
      ],
      "utmSource": [
        {}
      ],
      "utmTerm": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | array<object> |  |
| `city` | array<object> |  |
| `clicks` | number |  |
| `clicksPerLink` | string |  |
| `clicksPerLinkChange` | string |  |
| `clickStatistics` | object |  |
| `country` | array<object> |  |
| `device` | array<object> |  |
| `humanClicks` | number |  |
| `humanClicksChange` | string |  |
| `humanClicksChangePositive` | boolean |  |
| `humanClicksPerLink` | string |  |
| `interval` | object |  |
| `links` | number |  |
| `linksChange` | string |  |
| `linksChangePositive` | boolean |  |
| `loading` | boolean |  |
| `os` | array<object> |  |
| `prevClicks` | number |  |
| `prevClicksChange` | string |  |
| `prevHumanClicks` | number |  |
| `referer` | array<object> |  |
| `sample` | boolean |  |
| `social` | array<object> |  |
| `utmCampaign` | array<object> |  |
| `utmContent` | array<object> |  |
| `utmMedium` | array<object> |  |
| `utmSource` | array<object> |  |
| `utmTerm` | array<object> |  |

## Native endpoint

Through the native Short.io API, this operation is `GET https://statistics.short.io/statistics/domain/:domainId` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-statistics.md) for the provider-specific parameters and requirements.

