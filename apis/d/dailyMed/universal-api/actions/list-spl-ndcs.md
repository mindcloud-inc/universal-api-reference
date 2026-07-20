# DailyMed: List SPL NDCs

Retrieves NDCs for an SPL from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spl-ndcs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spl-ndcs?connectionId=$CONNECTION_ID&setid=4543e156-1deb-666e-e063-6394a90a719c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setid": "4543e156-1deb-666e-e063-6394a90a719c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spl-ndcs?${params}`, {
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
| `setid` | string | yes | The DailyMed SET ID of the SPL whose associated NDCs should be returned. Default: `4543e156-1deb-666e-e063-6394a90a719c`. Example: `4543e156-1deb-666e-e063-6394a90a719c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ndc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ndc` | string | National Drug Code associated with the SPL. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /spls/{setid}/ndcs.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spl-ndcs.md) for the provider-specific parameters and requirements.

