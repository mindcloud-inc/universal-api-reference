# Aspire: List Clock Times



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-clock-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-clock-times?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-clock-times?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedDateTime": {},
      "acceptedShortLunch": true,
      "acceptedUserID": {},
      "acceptedUserName": {},
      "breakTime": 1,
      "clockEnd": "string",
      "clockStart": "string",
      "clockTimeID": 1,
      "contactID": 1,
      "contactName": "Ava Chen",
      "gEOLocationEndLatitude": {},
      "gEOLocationEndLongitude": {},
      "gEOLocationStartLatitude": {},
      "gEOLocationStartLongitude": {},
      "preventedFromUsingBreaks": {},
      "usedBreaks": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedDateTime` | object |  |
| `acceptedShortLunch` | boolean |  |
| `acceptedUserID` | object |  |
| `acceptedUserName` | object |  |
| `breakTime` | number |  |
| `clockEnd` | string |  |
| `clockStart` | string |  |
| `clockTimeID` | number |  |
| `contactID` | number |  |
| `contactName` | string |  |
| `gEOLocationEndLatitude` | object |  |
| `gEOLocationEndLongitude` | object |  |
| `gEOLocationStartLatitude` | object |  |
| `gEOLocationStartLongitude` | object |  |
| `preventedFromUsingBreaks` | object |  |
| `usedBreaks` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET ClockTimes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clock-times.md) for the provider-specific parameters and requirements.

