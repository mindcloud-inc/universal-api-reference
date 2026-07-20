# FEMA: List NFIP Community Status Book

Retrieves the NFIP Community Status Book from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-community-status-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-community-status-book?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-community-status-book?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "classRating": "string",
      "communityIdNumber": "string",
      "communityName": "Ava Chen",
      "county": "string",
      "currentlyEffectiveMapDate": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "nonSfhaDiscount": 1,
      "participatingInNFIP": true,
      "regularEmergencyProgramDate": "string",
      "sfhaDiscount": 1,
      "state": "string",
      "tribal": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classRating` | string |  |
| `communityIdNumber` | string |  |
| `communityName` | string |  |
| `county` | string |  |
| `currentlyEffectiveMapDate` | string |  |
| `lastRefresh` | date |  |
| `nonSfhaDiscount` | number |  |
| `participatingInNFIP` | boolean |  |
| `regularEmergencyProgramDate` | string |  |
| `sfhaDiscount` | number |  |
| `state` | string |  |
| `tribal` | boolean |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/NfipCommunityStatusBook` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfip-community-status-book.md) for the provider-specific parameters and requirements.

