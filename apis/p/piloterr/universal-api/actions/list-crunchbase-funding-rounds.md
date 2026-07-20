# Piloterr: List Crunchbase Funding Rounds



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/list-crunchbase-funding-rounds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/list-crunchbase-funding-rounds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/list-crunchbase-funding-rounds?${params}`, {
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
| `daysSinceAnnouncement` | string | no | Limit rounds announced within the last N days. |
| `fundedOrganizationIdentifier` | string | no | Crunchbase organization UUID to filter rounds. |
| `investmentType` | string | no | Crunchbase funding round type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "identifier": {
          "value": "string"
        },
        "investmentType": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.identifier.value` | string |  |
| `results.investmentType` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /crunchbase/funding_rounds` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crunchbase-funding-rounds.md) for the provider-specific parameters and requirements.

