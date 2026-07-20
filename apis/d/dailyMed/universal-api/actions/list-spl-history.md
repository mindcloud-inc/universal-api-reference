# DailyMed: List SPL History

Retrieves SPL version history from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spl-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spl-history?connectionId=$CONNECTION_ID&setid=4543e156-1deb-666e-e063-6394a90a719c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setid": "4543e156-1deb-666e-e063-6394a90a719c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spl-history?${params}`, {
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
| `setid` | string | yes | The DailyMed SET ID of the SPL whose version history should be returned. Default: `4543e156-1deb-666e-e063-6394a90a719c`. Example: `4543e156-1deb-666e-e063-6394a90a719c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "published_date": "2026-05-07T12:00:00.000Z",
      "spl_version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `published_date` | date | Version publication date. |
| `spl_version` | number | SPL version number. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /spls/{setid}/history.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spl-history.md) for the provider-specific parameters and requirements.

