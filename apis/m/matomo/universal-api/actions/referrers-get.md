# Matomo: Get Referrers Overview



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/referrers-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/referrers-get?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/referrers-get?${params}`, {
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
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `period` | string | yes | Matomo API parameter. Default: `day`. |
| `date` | string | yes | Matomo API parameter. Default: `yesterday`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `segment` | string | no | Matomo API parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Referrers_distinctAIAssistants": 1,
      "Referrers_distinctCampaigns": 1,
      "Referrers_distinctKeywords": 1,
      "Referrers_distinctSearchEngines": 1,
      "Referrers_distinctSocialNetworks": 1,
      "Referrers_distinctWebsites": 1,
      "Referrers_visitorsFromAIAssistants": 1,
      "Referrers_visitorsFromAIAssistants_percent": 1,
      "Referrers_visitorsFromCampaigns": 1,
      "Referrers_visitorsFromCampaigns_percent": 1,
      "Referrers_visitorsFromDirectEntry": 1,
      "Referrers_visitorsFromDirectEntry_percent": 1,
      "Referrers_visitorsFromSearchEngines": 1,
      "Referrers_visitorsFromSearchEngines_percent": 1,
      "Referrers_visitorsFromSocialNetworks": 1,
      "Referrers_visitorsFromSocialNetworks_percent": 1,
      "Referrers_visitorsFromWebsites": 1,
      "Referrers_visitorsFromWebsites_percent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Referrers_distinctAIAssistants` | number | Matomo metric Referrers_distinctAIAssistants |
| `Referrers_distinctCampaigns` | number | Matomo metric Referrers_distinctCampaigns |
| `Referrers_distinctKeywords` | number | Matomo metric Referrers_distinctKeywords |
| `Referrers_distinctSearchEngines` | number | Matomo metric Referrers_distinctSearchEngines |
| `Referrers_distinctSocialNetworks` | number | Matomo metric Referrers_distinctSocialNetworks |
| `Referrers_distinctWebsites` | number | Matomo metric Referrers_distinctWebsites |
| `Referrers_visitorsFromAIAssistants` | number | Matomo metric Referrers_visitorsFromAIAssistants |
| `Referrers_visitorsFromAIAssistants_percent` | number | Matomo metric Referrers_visitorsFromAIAssistants_percent |
| `Referrers_visitorsFromCampaigns` | number | Matomo metric Referrers_visitorsFromCampaigns |
| `Referrers_visitorsFromCampaigns_percent` | number | Matomo metric Referrers_visitorsFromCampaigns_percent |
| `Referrers_visitorsFromDirectEntry` | number | Matomo metric Referrers_visitorsFromDirectEntry |
| `Referrers_visitorsFromDirectEntry_percent` | number | Matomo metric Referrers_visitorsFromDirectEntry_percent |
| `Referrers_visitorsFromSearchEngines` | number | Matomo metric Referrers_visitorsFromSearchEngines |
| `Referrers_visitorsFromSearchEngines_percent` | number | Matomo metric Referrers_visitorsFromSearchEngines_percent |
| `Referrers_visitorsFromSocialNetworks` | number | Matomo metric Referrers_visitorsFromSocialNetworks |
| `Referrers_visitorsFromSocialNetworks_percent` | number | Matomo metric Referrers_visitorsFromSocialNetworks_percent |
| `Referrers_visitorsFromWebsites` | number | Matomo metric Referrers_visitorsFromWebsites |
| `Referrers_visitorsFromWebsites_percent` | number | Matomo metric Referrers_visitorsFromWebsites_percent |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/referrers-get.md) for the provider-specific parameters and requirements.

